---

layout: gallery
title: Gallery
description:
keywords: brogue, gallery, screenshots, screengrabs
excerpt: Gratuitous screenshots 👍
exclude_from_nav:
gallery:
- image: dragonslayer.png
  title: Dragonslayer
  description: I killed a dragon
- image: captive-horrors.png
  title: Captive horrors
  description:
- image: ectoplasm.png
  title: Ectoplasm!
  description:
- image: explosion.png
  title: Explosion
  description:
- image: float.png
  title: Floaters
  description: All my stuff floats away
- image: gas.png
  title: Gas
  description: A dangerous build up of gas
- image: healthyhorror.png
  title: Healthy horror
  description: My tentacled horror looks better
- image: incineration.png
  title: Incineration
  description: Boiling the lake
- image: jellyfly.png
  title: Flying jellies
  description:
- image: jellysap.png
  title: Jelly sap
  description: Strength sapping jellies
- image: magic.png
  title: A kind of magic
  description: Lots of magical stuff here
- image: mangrove.png
  title: Mangrove liability
  description: Mangrove dryads are a liability
- image: oldfriend.png
  title: Old friend
  description: An old friend emerges
- image: rainbow-ring.png
  title: Rainbow ring
  description:
- image: steam-dead.png
  title: A mangrove dryad did this
  description:
- image: steam.png
  title: Scalding steam
  description:
- image: stranded.png
  title: Stranded aquatics
  description:
- image: zombies.png
  title: Zombies!
  description:
nav-class: gallery
permalink: /gallery/

---


<div class="gallery-container">
{% assign items = page.gallery | sort: 'date' %}
{% for gallery in page.gallery limit:200 %}
    <a class="seed-card" data-wenk="Click to enlarge" data-wenk-pos="bottom" title="{% if gallery.description %}{{ gallery.description }}{% else %}{{ gallery.title }}{% endif %}: full size" href="#{{ gallery.image }}">
        <img src="/screenshot-thumbs/thumb-{{ gallery.image }}" alt="{% if gallery.description %}{{ gallery.description }}{% else %}{{ gallery.title }}{% endif %}" class="seed-thumb"/>
        <h3 class="cf gallery-title seed-title-animate">{{ gallery.title }}</h3>
    </a>
{% endfor %}
</div>

{% assign items = page.gallery | sort: 'date' %}
{% for gallery in page.gallery limit:200 %}
<a href="#" class="lightbox" id="{{ gallery.image }}">
  <img src="/screenshots/{{ gallery.image }}" alt="{{ gallery.title }}" class="seed-thumb"/>
</a>
{% endfor %}