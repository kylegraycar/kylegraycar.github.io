---
layout: post
title: "Site Progress Check #1"
description: Everything I've done so far
date: 2015-11-24 13:12:00
featured_image: 
categories: website
tags: web development, jekyll, GitHub, static-site
---

I started working on this website late August 2015 as a means to familiarize myself with the world of coding and web development. It's generated with [Jekyll][] and hosted on [GitHub][]. I've learned a lot around HTML, CSS, and Markdown, but there's still much (much, much) more to learn. 

In this "progress check" I've listed all the features I've included in my site since it's inception and commented on the process. In general, I knew I wanted two things from this site:

1. Something minimalist and clean
2. Everything "from scratch" 
	
	Rather than importing a theme, I decided to begin with Jekyll's default settings and styling and try to build everything myself so that I could learn more from the process. I've hence realized that building everything myself was a lot more than I bargained for and nigh impossible for someone with as little experience as myself, so I've employed the help of sites like Flickr and Mailchimp and others as I'll explain below.

The List
--------
Here's everything I've added to my site:

 * A homepage
 * [Tsatchi][] Instagram widget to homepage
 * An about page
 * A resume page
 * Downloadable resume PDF
 * Modified footer content
 * Mailchimp email list to blog page
 * Flickr embedded photo slideshows for Snaps posts
 * Facebook, LinkedIn, and twitter share buttons
 * Commentit.io comments posting


The Details
-----------
Here's a closer look at my thoughts and procedures for those additions.


###Homepage###
The default Jekyll theme integrates the blog page and homepage into one. That is to say, there isn't really a homepage. This is common for most blogs and personal websites, but I wanted to feature a landing page that's more visually compelling. Before including the tsatchi Instagram plugin I simply included a favorite photo of mine that I had taken recently. I find this homepage to be a simpler way for users to be introduced to my site and then navigate to the blog or about page, rather than instantly being bombarded with the blog lists with vague seeming titles and no visual aesthetic.

I created this homepage by first creating a blog page, where I dumped the posts list snippet that was originally within `index.html`. This is Jekyll's post list code:

	<ul class="post-list" align="center">
    	{% for post in site.posts %}
      		<li>
        	<span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
        	<h2>
          	<a class="post-link" href="{{ post.url | prepend: site.baseurl }}">{{ post.title }}</a>
        	</h2>
        	<p>
          	{{ post.description }}
        	</p>
      		</li>
    	{% endfor %}
    </ul> 

Note: Jekyll will locally break this HTML into both HTML and the [Liquid][] templating language. NEED TO FIX THIS. 

From there, my `index.html` was blank and I filled it with the tsatchi Instagram plugin descried below.

###Tsatchi Instagram widget to homepage###
As I mentioned above, I wanted my homepage to be visual and simplistic, so originally I simply embedded a favorite photo of mine. That's when I realized I already did that all the time with Instagram. That began my hunt for a single image Instagram widget. I chose [Tsatchi][]'s Instagram widget for the following reasons:

* It has a neat Javascript for hover and slideshow animating
* Clicking on the image links directly to the photo on Instagram, not a 3rd party
* It's automatic and instantaneous - I could have used a Flickr slideshow but would have had to manually upload the photo and put it in an album.

I've only found two drawbacks:

* Long load time (partially due to my location, China)
* The size of the widget does not change with the size of the user's window - I'm still looking into this..

###An about page###

###A resume page (includes downloadable PDF)###

###Downloadable resume PDF###

###Modified footer content###

###Mailchimp email list to blog page###

###Flickr embedded photo slideshows for Snaps posts###

###Facebook, LinkedIn, and twitter share buttons###

###Commentit.io comments posting###

[Jekyll]: https://jekyllrb.com
[GitHub]: https://github.com/kylegraycar
[Liquid]: https://github.com/Shopify/liquid/wiki
[Tsatchi]: http://tsatchi.com/instagram-widget-builder
