---
layout: post
title: "Jekyll Excerpt Hack for Github Pages"
description: ""
category: 
tags:
- jekyll
- github
- hacks
---

I have just recently migrated my old WordPress blog to Jekyll and hosted
it on Github pages. I don't know if Github's Jekyll supports excerpt or not,
I just know that it disables any custom plugin using `--safe` flag. 

At first, I decided to list only the post titles in the front page, but
I just realized that it was bad decision.  I don't like to throw up my posts' 
whole content to the index page, and of course prefer *excerpt* instead.

<!-- more -->

After a little googling, I found a solution by 
[Kaspars](http://kaspa.rs/2011/04/jekyll-hacks-html-excerpts/)
that involves replacing a comment `<!-- more start -->` and `<!-- more end -->` 
tags with zero-length string to mark the start and end of the rest of the 
content leaving the excerpt to be displayed by browser.


---


I feel odd with that workaround and quickly find out a (slightly) better 
approach to this.

Here's the Liquid syntax I used to display the excerpt:

{% highlight text %}
{{ "{{ post.content | split:'<!-- more -->' | first " }}}}
{% endhighlight %}

Then insert the usual more tag to your markdown post:

{% highlight text %}
This is an excerpt. Lorem ipsum dolor sit amet, consectetur adipisicing elit, 
sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim 
ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip 
ex ea commodo consequat. 
 
<!-- more -->
 
The rest of the content goes here. Duis aute irure dolor in reprehenderit 
in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur 
sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt 
mollit anim id est laborum.
{% endhighlight %}

The plus of this method is the similiar syntax with WordPress' "more" links ;)