---
layout: splash
permalink: /
title: "Home"
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/core/home.jpg
  logo_header: /assets/images/core/logo_full_inverse.png
  logo_background: /assets/images/core/logo_full.png
#  cta_label: "<i class='fa fa-gear'></i> UE4 Marketplace"
#  cta_url: "https://www.unrealengine.com/marketplace/profile/Cronofear%20Softworks"
  caption: ""
#excerpt: 'Games and Tools Development in Unreal Engine 4.'
description: 'Games and Tools Development in Unreal Engine 4.'
descsize: '82%'
descref: '#featured'
intro:
  - excerpt: '<a style="font-size: 75%;">Follow me on:</a>
  [<i class="fa fa-facebook"></i>](https://www.facebook.com/Cronofear/){: .btn .btn--light-outline .btn--small}
  [<i class="fa fa-twitter"></i>](https://twitter.com/cronofearSW){: .btn .btn--light-outline .btn--small}
  [<i class="fa fa-youtube-play"></i>](https://www.youtube.com/channel/UCTE-TAOV8uGyX5ITofi93Ew){: .btn .btn--light-outline .btn--small}
  [<i class="fa fa-tumblr"></i>](https://cronofearsoftworks.tumblr.com/){: .btn .btn--light-outline .btn--small} 
  [<i class="fa fa-paypal"></i>](https://www.paypal.me/cronofear){: .btn .btn--light-outline .btn--small}'
share:
  - excerpt: '<a style="font-size: 75%;">Share on:</a>
  [<i class="fa fa-facebook"></i>](https://www.facebook.com/Cronofear/){: .btn .btn--light-outline .btn--small}
  [<i class="fa fa-twitter"></i>](https://twitter.com/cronofearSW){: .btn .btn--light-outline .btn--small}
 [<i></i>Subscribe](#subscribe){: .btn .btn--light-outline .btn--small}'
feature_row:
  - image_path: /assets/images/game_assets/save_system/logo.png                           #FEATURED IMAGE 1 500x280
    alt: "Buy Plug-in"
    title: "[Asset] Autosave & Load w/ compression"
    excerpt: "Easy to use, useful and flexible Plug-in that will allow you to implement a Save and Load system in your games. In a breeze!"
    url: "https://www.unrealengine.com/marketplace/csw-autosave-and-load-system-w-compression"
    btn_class: "btn--primary"
    btn_label: "Learn More"
    url2: "/docs-save-load-system/welcome/" #if commented, don't show button
    btn_class2: "btn--primary"
    btn_label2: "Documentation" 
feature_row2:
  - image_path: /assets/images/game_assets/level_makr/logo.jpg                            #FEATURED IMAGE 2 500x280
    alt: "Buy Plug-in"
    title: "[Asset][WIP] Level Makr Kit"
    excerpt: "Incredible Level Editor set of tools for Unreal Engine 4. Craft your games and give your players the ability to create and share their own levels!"
    url: "https://www.facebook.com/Cronofear/"
    btn_class: "btn--primary"
    btn_label: "Follow"
    #url2: "" #if commented, don't show button
    btn_class2: "btn--primary"
    btn_label2: "Learn More" 
---

<a id="featured">
<!-- Featuring -->
{% include feature_row.html id="feature_row" type="left" %}
{: .notice--primary}
{% include feature_row.html id="feature_row2" type="right" %}
{: .notice}

{% comment %}
<!-- Listing Assets -->
<a id="gameassets">
# <i class="fa fa-plug"></i> UE4 Assets
{: .text-center}
<div class="grid__wrapper" style="height:auto; overflow:auto">
  {% for post in site.gameassets limit:4 %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
***

<!-- Listing Games -->
<a id="games">
# <i class="fa fa-gamepad"></i> Games
{: .text-center}
<div class="grid__wrapper" style="height:auto; overflow:auto">
  {% for post in site.games limit:4 %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>
***
{% endcomment %}
***
<!-- Listing Blog -->
<a id="blog">
# <i class="fa fa-coffee"></i> Latest in the Blog
{: .text-center}
<div class="grid__wrapper" style="height:auto; overflow:auto">
  {% for post in site.posts limit:4 %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>