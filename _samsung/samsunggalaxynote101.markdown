---
layout: device
title:  "Samsung Galaxy Note 10.1"
codename: p4noterf
downloadfolder: "n8000|n8000|n8010|n8010|n8020|n8020"
supportstatus: Current
maintainer: html6405
oem: Samsung
devicetree: "https://github.com/TeamWin/android_device_samsung_n8000"
ddof: "/dev/block/bootdevice/by-name/recovery"
---

{% include disclaimer.html %}

{% include supportstatus.html %}

{% include appinstall.html %}

<div class='page-heading'>Download Links:</div>
<hr />
<p class="text">n8000:</p>
<ul>
{% for mirror in site.data.mirrors %}
  <li>
    <a href="{{ mirror.baseurl }}n8000">
      {{ mirror.description }}
    </a>
  </li>
{% endfor %}
</ul>
<p class="text">n8010:</p>
<ul>
{% for mirror in site.data.mirrors %}
  <li>
    <a href="{{ mirror.baseurl }}n8010">
      {{ mirror.description }}
    </a>
  </li>
{% endfor %}
</ul>

<p class="text">n8020:</p>
<ul>
{% for mirror in site.data.mirrors %}
  <li>
    <a href="{{ mirror.baseurl }}n8020">
      {{ mirror.description }}
    </a>
  </li>
{% endfor %}
</ul>

{% include twrpinstall.html %}

{% include odininstall.html %}

{% include ddinstall.html %}
