---
layout: post
title: Tracking Home Climate with TRMNL
date: 2025-7-19
location: Toronto, Canada
author: Murdo
---

Toronto is being scorched this summer. 

---

I’ve learned more about airflow, humidity, and AC units than I ever planned to. I’ve always been a PPM guy, though. With a couple of temperature and humidity sensors already placed around the house, I wanted a more immediate sense of our airflow feedback loop. In a quiet stretch during parental leave, I built another TRMNL plugin. 

There are a variety of reasons you might feel uncomfortable inside during a hot summer. High humidity makes your space feel sticky and muggy, even if the temperature is fine. Stale air can trap heat, creating hot pockets that catch you off guard. It’s especially important to watch for in bedrooms you want cool at night but don’t frequent during the day. Then there’s the potential for headaches when humidity, temperature, and poor air quality combine to overwhelm the senses. 

<figure>
  <img class="blogImage" src="/assets/blogimg/trmnl-home.png" alt="plugin on device">
</figure>

By combining HomeKit data, automated iOS shortcuts, Google App Scripts (an often forgotten but incredibly reliable tool), and my little TRMNL device, I now have a simple way to understand our home. Mostly, I’ve learned that opening windows isn’t always the fix you think it’ll be. 

The architecture is relatively simple:
1. Every hour, an iOS automation runs the data-gathering shortcut, collecting temperature, humidity, and air quality across our main floor and upstairs.
2. The shortcut passes all of this timestamped data as a JSON blob to an App Script that places it into a Google Sheet. 
3. Every 15 minutes, the Google Sheet is parsed as a CSV by my custom TRMNL plugin, slicing to retrieve only the last 24 readings before plotting the time series. 

Timezone conversion was a rabbit hole. In the end, hard-coding the time was the simplest fix. It won’t scale beyond my setup, but it works exactly as needed.

It’s by no means real-time. But it’s passively available, easily accessible to other tools, and uses aging tech that (hopefully) resists the brittleness of new systems. 

You can view my App Scripts code [here](https://gist.github.com/Murdo-C/f7e160993899861e0118afd58f29cff2), iOS shortcut steps [here](/assets/blogimg/shortcut-home-status.jpg), and TRMNL code [here](https://gist.github.com/Murdo-C/185462ea9fe4475f079f6fd9075e6361).

Time-based iOS shortcut automations aren’t natively supported. But I stumbled across [this](https://www.reddit.com/r/shortcuts/comments/t6puvi/comment/hzfymhp/) brilliant hack using a global ‘runner’ shortcut. It takes a bit of setup, but offers a repeatable way to run any shortcut on a schedule.

I’m letting this version settle before adding new features. I’m considering outside temperature integration, more frequent measurements, and a forecast view powered by a simple indoor temperature model I’ve yet to explore. 

I’ve always had an intuitive sense of how to do technical things. TRMNL pairs with that instinct, allowing me to quickly turn small ideas into real tools.
