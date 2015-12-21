---
layout: post
title: "Installing Rails in China"
description: Your VPN won't help
date: 2015-12-21 11:59:00
featured_image: /assets/RubyCourseComplete.jpg
categories: website
tags: web development, Ruby, Ruby on Rails, VPN, install rails
---
For my next phase of learning Rails, I've decided to go through all the [free guides][] on the Rails website. I'll write more about them once I complete the first "Getting Started" guide, but in order to use these guides I first had to actually install Rails. I know what you're thinking... "Just type `$ gem install rails` into terminal, what's the issue?" 

Well, China's the issue. More specifically, the [Great Firewall][]. This isn't anything new to westerners here, we just use a [VPN][] (Virtual Private Network) to access essential sites like Facebook, Google, Instagram, and Netflix.

Unfortunately just turning on your VPN and and entering `$ gem install rails` doesn't work. You'll get this error message:

	$ gem install rails
	ERROR:  While executing gem ... (Gem::RemoteFetcher::FetchError)
	    Errno::ECONNRESET: Connection reset by peer - SSL_connect (https://rubygems.org/quick/Marshal.4.8/loofah-2.0.3.gemspec.rz)

Or this one:

	$ gem install rails
	ERROR:  While executing gem ... (Gem::RemoteFetcher::FetchError)
	    Errno::ETIMEDOUT: Operation timed out - connect(2) for "rubygems.global.ssl.fastly.net" port 443 (https://rubygems.org/quick/Marshal.4.8/loofah-2.0.3.gemspec.rz)

Or the terminal marker will just hang there and you won't get any response or error message.

So, with or without a VPN the install won't work. It turns out the solution is more nuanced than I thought. The database for Rails and other Ruby gems are stored on [Amazon S3][], which is of course blocked by the Great Firewall. I found this great [Chinese website][] that explains how to install Rails, bundle, and other gemfiles using a mirrored database stored in taobao.org (which also happens to essentially be the Amazon of China).

The trick is to switch the source of the install from Amazon to Taobao. Here's how:

	$ gem sources --add https://ruby.taobao.org/ --remove https://rubygems.org/
	https://ruby.taobao.org/ added to sources
	https://rubygems.org/ removed from sources

Now, check your source:

	$ gem sources -l
	*** CURRENT SOURCES ***

	https://ruby.taobao.org/

Finally, with your VPN turned off, `$ gem install rails`. That should do the trick! Welcome aboard!

![welcome-aboard][]

[free guides]: http://guides.rubyonrails.org/getting_started.html
[Great Firewall]: https://en.wikipedia.org/wiki/Great_Firewall
[VPN]: https://en.wikipedia.org/wiki/Virtual_private_network
[Amazon S3]: http://docs.aws.amazon.com/AmazonS3/latest/dev/Welcome.html
[Chinese website]: https://ruby.taobao.org

[welcome-aboard]: /assets/welcome-aboard.png