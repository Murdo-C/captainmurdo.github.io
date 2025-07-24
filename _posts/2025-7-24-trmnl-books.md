---
layout: post
title: Discover a Timeless Ebook Every Day on TRMNL
date: 2025-7-24
location: Toronto, Canada
author: Murdo
---

Each day my plugin serves up one carefully curated, public-domain ebook from [Standard Ebooks](https://standardebooks.org). 

---

Choose from all genres, a curated few, or just your favourite. Free, beautifully formatted, timeless texts delivered straight to your TRMNL.

<figure>
  <img class="blogImage" src="/assets/blogimg/trmnl-book.png" alt="plugin on device">
</figure>

Timeless Texts was my entry to the TRMNL book reader [hackathon](https://usetrmnl.com/blog/hackathon-book-readers). Building plugins continues to be a great evening project during my parental leave. The hackathon provided a focused challenge. The consistency and craft behind Standard Ebooks made it the perfect foundation to build on.

With this one, I was interested in exploring an external API. Standard Ebooks offers an [OPDS feed](https://standardebooks.org/feeds), which they make available to open source projects. I wanted to respect the API and avoid exposing all of Standard Ebooks’ feed details to the public. So inadvertently, I found myself building my own API. My API uses Standard Ebooks’ feed to select one book from their entire catalog, plus one from each of their 19 genres - for a total of 20 randomly selected books. It runs daily via GitHub Actions to create a books.json that I can then access via TRMNL’s plugin framework.

I’m particularly proud of three plugin features:
1. It supports all available size classes, gracefully scaling down while keeping a cover-focused layout. 
2. I wanted users to instantly access the books they see. Generating a QR code for the displayed book allows you to go from passive interest to active reading in seconds.
3. I initially showed the same book to all users. Good, but not great. Adding genre personalization wasn’t easy. I had to shift from a single JSON array to parsing pools of options from a much longer list, but the result is clearly better.

While the API is hosted on GitHub, I wanted the plugin output to be generated client-side. It’s built using Liquid, JavaScript, HTML, and Tailwind-style CSS. I’ve enjoyed getting to know Liquid’s quirks through TRMNL projects. Thankfully, there’s plenty of Shopify-built content to help.

The plugin is now available for TRMNL users. The code is open source in the ``standard-ebooks-daily`` [repo](https://github.com/Murdo-C/standard-ebooks-daily/). Fork the code, use the API, and reach out if you build something cool. 
