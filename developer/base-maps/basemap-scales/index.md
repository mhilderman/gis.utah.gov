---
title: Online Base Map Scale Information
author:
  display_name: Steve Gourley
  email: sgourley@utah.gov
tags:
  - basemap
  - cache
date: 2011-08-04 23:56:06 -0600
categories: []
---
![scale bar]({{ "/images/scales.png" | prepend: site.baseurl }}){: .pull-right} With the move to web mercator we are moving into a global scale level world. The base map services that we offer fall in between the world view, _scale 0_, and the much more zoomed in manhole cover scale - _20_. The table below describes the base map that we offer with it's min and max zoom levels. The table below that describes the scale to which that zoom level is equivalent to.

Handling these different scales requires some extra effort within the esri javascript api version 3.x. In order to make these services accessible and easy to work with we have created the [layer selector](https://github.com/agrc-widgets/layer-selector) widget. You can read more about this widget and examples of it's use in [this blog post]({{site.baseurl}}{% post_url 2015-12-21-using-agrcs-new-web-mercator-services-in-your-web-maps %}) or you can browse to [atlas.utah.gov](https://atlas.utah.gov) to see it in action.

| Base map | Min Zoom | Max Zoom |
|:---------|:--------:|---------:|
| Color IR | 0 | 18 |
| Imagery | 0 | 20 |
| Lite | 5 | 19 |
| Overlay | 5 | 19 |
| Terrain | 5 | 19 |
| Topo | 5 | 17 |
|===
{: style="width:auto"}

| Zoom | Scale |
|--:|:--|
| 20 | 1128.497220 |
| 19 | 2256.994440 |
| 18 | 4513.988880 |
| 17 | 9027.977761 |
| 16 | 18055.955520 |
| 15 | 36111.911040 |
| 14 | 72223.822090 |
| 13 | 144447.644200 |
| 12 | 288895.288400 |
| 11 | 577790.576700 |
| 10 | 1155581.153000 |
| 9 | 2311162.307000 |
| 8 | 4622324.614000 |
| 7 | 9244649.227000 |
| 6 | 18489298.450000 |
| 5 | 36978596.910000 |
| 4 | 73957193.820000 |
| 3 | 147914387.600000 |
| 2 | 295828775.300000 |
| 1 | 591657550.500000 |
|  0 | 5 9 1 6 5 7 5 5 0 . 5 0 0 0 0 0  |
|==
{: style="width:auto"}
