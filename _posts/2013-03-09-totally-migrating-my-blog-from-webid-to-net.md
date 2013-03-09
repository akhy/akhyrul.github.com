---
layout: post
title: "Totally Migrating My Blog from .web.id to .net"
description: ""
category: 
tags:
- hosting
- domain
- tips
---

One suck thing about using .web.id domain is unability to manually manage DNS.
I'm not pretty sure, but my hosting company's customer service told me so. 
One of the impact is that I cannot change "A record" to serve my root domain
(not the www-prefixed one) from Github pages.

So I decided to move my Jekyll powered blog to this .net domain I own. Just
for SEO reason, I try all my best to preserve all the blog permalinks. 
My preferred way was to redirect all the request from the old domain to the
new one using "HTTP 301 Redirect" (Permanently moved), so search engine bots
would know that my contents no longer reside there.

Here's the  .htaccess file I put on my old domain's root:

{% highlight text %}
RewriteEngine On
RewriteRule (.*) http://akhyar.net/$1 [L,R=301]
{% endhighlight %}

That way, all request to akhyar.web.id will be redirected to the new domain
at akhyar.net.

