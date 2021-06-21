:github_url:  https://github.com/transportkollektiv/digitransit-setup/tree/main/src/installation/faq.rst

Frequently Asked Questions
==========================

-  **I see no frequently asked questions?!** – Feel free to ask one :)
-  **I did everything as you say, but when I test bus relations, the route
   is all zigzagging over the map instead of following the road**
   –  Your :term:`GTFS` feed is missing ``shapes.txt``. This happens 
   occasionally, depending on where you get your feed from. See `this blog
   post <https://ulm.dev/2020/01/17/pfaedle/>`_ on how to integrate
   them into your feed yourself
-  **The time zone is off: Routing results are as many hours ahead/behind of the desired time as my local time zone is ahead/behind of UTC, how coincidental!**
   - For whatever reason, digitransit insists on delivering its own ``timezoneData`` within ``config.js``. Whenever this definition expires, your timezone will be off. Replace the text string with the one fitting your time zone from `github.com/moment/moment-timezone/blame/develop/data/packed/latest.json <https://github.com/moment/moment-timezone/blame/develop/data/packed/latest.json>`_ to realign yourself within the correct space-time. (See `this diff <https://github.com/stadtnavi/digitransit-ui/commit/0b2f614e8929802803373c5eda605080cd9c3f57>`_ for comparison and explanation)
