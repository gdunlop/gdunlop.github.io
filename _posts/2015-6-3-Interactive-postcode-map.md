---
layout: post
title: Interactive postcode map
---
An interactive map of 1.6 million postcodes in Great Britain using [Tableau Public](https://public.tableau.com/s/) prompted by [a tweet from Brian Timoney](https://twitter.com/briantimoney/status/605430821730684928). I'm increasingly turning to statistical and analytical tools to manipulate and visualise large geospatial datasets, and Tableau proves very capable in this respect.

Read the background to this project or skip right to the end to see the map.

### Inspiration

Several years ago I read Ben Fry's book [Visualizing Data](http://www.amazon.co.uk/exec/obidos/ASIN/0596514557/ref=nosim/benfrycom-20) and was impressed by `zipdecode` - an [interactive zipcode tool](http://benfry.com/zipdecode/) built using Processing. It was a simple dots-on-a-map visualisation of all US zipcodes with an added &quot;wow&quot; factor - start typing a zipcode and the map would zoom in/out and all matching zipcodes would light up.

![Interactive zipcodes using Processing]({{ site.baseurl }}/images/zip-decode.png)

### Perspiration

Around this time I recruited an intern into OS Labs for 6 weeks - Joseph Braybrook. He mentioned Minecraft during interview, so naturally the first task I set him was to [build a Minecraft version of Great Britain](http://www.ordnancesurvey.co.uk/innovate/developers/minecraft-map-britain.html). The result got some great press coverage and the story has a happy ending as Joe took on a permanent role with OS.

The remainder of Joe's internship was spent re-creating the  `zipdecode` use case incorporating OS mapping and postcode data. This worked great as a desktop application built in Processing but performance wasn't great and there was no chance of getting it working in a web browser.

![Interactive postcodes using Processing]({{ site.baseurl }}/images/postcode-finder.png)

### Exasperation

In the meantime I've played around with a lot of geo and web code libraries, platforms and applications and the &quot;interactive postcode map&quot; is my favoured use case - after all, how hard can it be to build a performant web map that is capable of handling millions of features with a high degree of interactivity?

Pretty hard it turns out, especially if you have seldom-used programming muscles like me and want to minimise your investment (time and money).

As a big fan of [Eric Fischer](https://www.mapbox.com/about/team/#eric-fischer) I've got pretty well into the Mapbox tools creating [things like this](http://gdunlop.github.io/Vector-maps-in-the-browser) along the way. I managed to use [tippecanoe](https://github.com/mapbox/tippecanoe) to build vector tilesets containing millions of points but couldn't figure out how to get the interactivity I was looking for. I also have no idea how to pronounce &quot;tippecanoe&quot;.

Next up I tried [CartoDB](https://cartodb.com/) which I've used successfully for lots of other map visualisation projects, which meant I hit the 50MB limit on their free plan very quickly and was not inclined to take on a paid subscription.

### Tribulation

Which brings me to Tableau. In the space of an hour I was able to sign up to [Tableau Public](https://public.tableau.com/s/), load up the Code-Point Open data and build a simple map view with wildcard search on postcode. There's a generous 10GB of storage on the free tier and a polished desktop app which I downloaded on OS X.

Tableau's map stack is by Stamen and provides a good selection of styling and content options. The only data preparation required was to transform Code-Point Open co-ordinates to web mercator using the geospatial Swiss Army knife that is `ogr2ogr` (other brands of geospatial utility knife are available).

### Visualisation

If you read this this far, thanks for reading. Here's the map...

<script type='text/javascript' src='https://public.tableau.com/javascripts/api/viz_v1.js'></script><div class='tableauPlaceholder' style='width: 540px; height: 720px;'><noscript><a href='http:&#47;&#47;gdunlop.github.io&#47;Interactive-postcode-map'><img alt='Interactive postcode map' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Bo&#47;Book1_3180&#47;cp-map&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz' width='540' height='720' style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='site_root' value='' /><param name='name' value='Book1_3180&#47;cp-map' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Bo&#47;Book1_3180&#47;cp-map&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='showVizHome' value='no' /><param name='showTabs' value='y' /><param name='bootstrapWhenNotified' value='true' /></object></div>
