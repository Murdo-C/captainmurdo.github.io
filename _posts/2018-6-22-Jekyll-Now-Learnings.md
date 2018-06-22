---
layout: post
title: My Jekyll Learnings
---

I recently set out to rebuild my (this) blog using open web standards whilst learning a thing or two along the way. 

Inspired by a friend, I wanted to figure out a bit of CSS, explore Markdown and dust off some HTML skills. The blog you're reading this on is the work in progress (and will continue to be, so you can judge for yourself as to how I'm doing). Regardless, I learned some interesting things during set-up and wanted to pass them along in case they help others. 

The main topics I cover here are:

1. [Jekyll](#jekyll)
2. [Redirecting a Squarespace domain to a GitHub Pages website](#domain-redirect)
3. [Favicons](#favicons)
4. [Search Engine Indexing](#SEO)
5. [Setting up Google Analytics](#analytics)

---

## Jekyll & Jekyll Now {#jekyll}
My journey began with [this](http://smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/) excellent Smashing Magazine guide for [Jekyll Now](https://github.com/barryclark/jekyll-now). I was previously running my blog via Squarespace, which came with two key pain points for me:

1. The back-end content management system was sluggish and didn't mesh nicely with my brain.
2. Using a template blog design meant I inherited too much complexity and wasn't learning anything through the process.

So when I stumbled upon the Smashing Magazine post, I instantly knew this was a much better way to address my need and solve those two pain points. The simplicity of static blogging, hosted through GitHub Pages, fits very nicely with my initial ambitions for this and the guide had me up and running in minutes. With a few basic tweaks to the design I already had something that felt like it belonged to me.

Starting down the Jekyll rabbit hole lead me to [Prose](http://prose.io), [Liquid](https://shopify.github.io/liquid/), [Bootstrap](https://getbootstrap.com), [React](https://reactjs.org) and more. But I'm taking this one step at a time and only tugging on the strings that I really need to explore.

## Redirecting Squarespace {#domain-redirect}
Continuing with the guide then led me to redirecting my existing Squarespace domain to the GitHub Pages domain. Unfortunately this was the only part of the guide that let me down and I had to troubleshoot a little.

Updating the CNAME as described wasn't quite enough; I also had to configure my `A` records within the Squarespace domain management dashboard. Thankfully GitHub has a number of support documents to help and [this one](https://help.github.com/articles/troubleshooting-custom-domains/#dns-record-doesnt-point-to-githubs-server) solved it for me.

With both the CNAME and `A` records set up to redirect it was simply a matter of waiting for the change to propagate across the globe.

>One thing I discovered while troubleshooting this part was how cheap [Google Domains](https://domains.google/) seems to be. Have a look if you're interested in setting up a blog similar to this.

## Favicons {#favicons}
I'm a great believer in getting the details right and the first thing on my list was to update the favicon. This little bit of customisation gave me the tiny jumpstart I needed to begin aligning the overall theme with my general design tastes and was a good way to help me quickly navigate to the Safari tab containing my blog whilst I edited.

![Safari Tabs](/images/safari-tabs.png)

Using [RealFaviconGenerator](https://realfavicongenerator.net) I was able to upload my standard **//**{: style="color: darkBlue"} logo, `hex #4183c4` naturally, and generate the required selection of favicons. Adding the files into my site's GitHub repo and updating my `default.html` layout with the provided HTML code was all it took to tick the first piece of customisation off my list.

From there, I began delving into the `style.scss` file to tinker. Sass/CSS is the first area I really want to explore and understand properly and the sheer volume of guides and explainers on these topics will keep me busy for ~~months~~ years.

## Search Engine Indexing {#SEO}
My name is already well optimised for search engines. Ideally though, this website would feature higher than my other online presences. I understand this takes a little bit of time, requiring this blog to (1) be indexed by Google and (2) for some traffic to accumulate here, but there are ways to help this along. 

Again, GitHub's support documentation has [simple instructions](https://help.github.com/articles/search-engine-optimization-for-github-pages/) to enable search engine optimisation (SEO) for Jekyll-based sites. It also helps to submit your URL to Google's [Search Console](https://www.google.com/webmasters/tools/home) to spur on the indexing.

There's more I can do here but this isn't a priority for now. I'm happy to let traffic arrive organically as I slowly move forward the development and content of my site.

## Google Analytics {#analytics}
The final piece to discuss is analytics. I wanted something lightweight and non-intrusive for visitors. Luckily, Jekyll Now includes support for Google Analytics. All that's required is to add the tracking code from Google to the `_config.yml` file. That's it. 

You can do some further tweaking within [Google Analytics](https://analytics.google.com/), such as linking your analytics to your search console account, to give you slightly more data on incoming traffic. As with SEO, this isn't a priority for me but I am curious to see what comes through from the first month of this site being live.
