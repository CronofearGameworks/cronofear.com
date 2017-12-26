---
layout: splash
permalink: /home
header:
  overlay_color: "#5e616c"
  overlay_image: /assets/images/core/home.jpg
  cta_label: "<i class='fa fa-gear'></i> UE4 Marketplace"
  cta_url: "https://www.unrealengine.com/marketplace/profile/Cronofear%20Softworks"
  caption:
excerpt: 'Games and Tools Development in Unreal Engine 4.'
feature_row:
  - image_path: /assets/images/ue4_assets/save_plugin/logo.png                           #FEATURED IMAGE 1
    alt: "Buy Plug-in"
    title: "[Asset] Autosave & Load w/ compression"
    excerpt: "Easy to use, useful and flexible Plug-in that will allow you to implement a Save and Load system in your Games. In a breeze!"
    url: "https://www.unrealengine.com/marketplace/csw-autosave-and-load-system-w-compression"
    btn_class: "btn--primary"
    btn_label: "Learn More"
feature_row2:
  - image_path: /assets/images/ue4_assets/level_makr/logo.jpg                            #FEATURED IMAGE 2
    alt: "Buy Plug-in"
    title: "[Asset][WIP] Level Makr Kit"
    excerpt: "Incredible Level Editor set of tools for Unreal Engine 4. Craft your games with the ability to create and share levels!"
    url: "https://www.facebook.com/Cronofear/"
    btn_class: "btn--primary"
    btn_label: "Follow"
feature_row3:
  - image_path: /assets/images/ue4_assets/save_plugin/logo.png                           #FEATURED IMAGE 1
    alt: "Buy Plug-in"
    title: "[Asset] Autosave & Load w/ compression"
    excerpt: "Easy to use, useful and flexible Plug-in that will allow you to implement a Save and Load system in your Games. In a breeze!"
    url: "https://www.unrealengine.com/marketplace/csw-autosave-and-load-system-w-compression"
    btn_class: "btn--primary"
    btn_label: "Learn More"
  - image_path: /assets/images/ue4_assets/level_makr/logo.jpg                            #FEATURED IMAGE 2
    alt: "Buy Plug-in"
    title: "[Asset][WIP] Level Makr Kit"
    excerpt: "Incredible Level Editor set of tools for Unreal Engine 4. Craft your games with the ability to create and share levels!"
    url: "https://www.facebook.com/Cronofear/"
    btn_class: "btn--primary"
    btn_label: "Follow"
  - image_path: /assets/images/ue4_assets/level_makr/logo.jpg                            #FEATURED IMAGE 3
    alt: "100% free"
    title: "[Tutorial] How to make a Plugin in Unreal Engine 4"
    excerpt: "A videotutorial about making a plugin in UE4! Hotreloaded is supported with this method"
    url: "https://www.youtube.com/watch?v=jvkFrETmCoA&list=PL7Se41ZzAKZmvCeW9iBpEuh_hxD7bMqMF"
    btn_class: "btn--primary"
    btn_label: "Learn More"
intro:
  - excerpt: 'Follow me on: &nbsp; 
  [<i class="fa fa-facebook"></i> Facebook](https://www.facebook.com/Cronofear/){: .btn .btn--facebook}
  [<i class="fa fa-youtube-play"></i> Youtube](https://www.youtube.com/channel/UCTE-TAOV8uGyX5ITofi93Ew){: .btn .btn--danger} 
  [<i class="fa fa-twitter"></i> Twitter](https://twitter.com/cronofearSW){: .btn .btn--twitter} 
  [<i class="fa fa-paypal"></i> Tip Me](https://www.paypal.me/cronofear){: .btn .btn--primary}'
---
{% include feature_row id="intro" type="center" %}
# FEATURED
{: .text-center}
***
{% include feature_row id="feature_row" type="left" %}
{% include feature_row id="feature_row2" type="right" %}
{% include feature_row id="feature_row3" %}

# PORTFOLIO
{: .text-center}
<div class="grid__wrapper">
  {% for post in site.portfolio %}
    {% include archive-single.html type="grid" %}
  {% endfor %}
</div>