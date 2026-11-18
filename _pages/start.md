---
layout: splash
permalink: /
hidden: true
classes: home-page
header:
  overlay_color: "rgb(0, 40, 150)"
  overlay_image: 
  show_overlay_excerpt: false
video_path: /assets/videos/intro.mp4
excerpt: >
  Das Zentrum für Robotik an der Hochschule Heilbronn ist eine interdisziplinäre Einrichtung, die sich der Forschung, Lehre und praxisnahen Entwicklung innovativer Lösungen im Bereich der Robotik widmet. <br />
  Im Fokus stehen moderne Technologien wie kollaborierende Robotersysteme (Cobots), künstliche Intelligenz in der Robotik sowie die klassische Industrierobotik. Studierende erhalten die Möglichkeit, in modernen Laboren praxisnahe Erfahrungen zu sammeln und an aktuellen Forschungsprojekten mitzuwirken – von der Konzeption über die Programmierung bis hin zur Umsetzung realer Anwendungen.
feature_row:
  - image_path: /assets/images/pks.png
    alt: "PKS"
    title: |
      Parallelkinematische Systeme
    excerpt: "Everything from the menus, sidebars, comments, and more can be configured or set with YAML Front Matter."
  - image_path: /assets/images/embodied_ai.jpg
    alt: "embodied AI"
    title: |
      Embodied AI
    excerpt: "Built with HTML5 + CSS3. All layouts are fully responsive with helpers to augment your content."
  - image_path: /assets/images/ros.png
    alt: "pks+ros"
    title: |
      ROS2
    excerpt: "Free to use however you want under the MIT License. Clone it, fork it, customize it... whatever!"    
---

<section class="home-intro" aria-label="Einführung und Video">
  <div class="home-intro__text">
    {{ page.excerpt | markdownify }}
  </div>
  {% assign video_file = site.static_files | where: "path", page.video_path | first %}
  {% if video_file %}
  <div class="home-intro__video">
    <video autoplay muted playsinline loop controls preload="metadata">
      <source src="{{ page.video_path | relative_url }}" type="video/mp4">
      Dein Browser unterstützt das Videoelement nicht.
    </video>
  </div>
  {% else %}
  <div class="home-intro__video-placeholder" role="img" aria-label="Video-Platzhalter im Format 16:9">
    <span class="home-intro__play" aria-hidden="true"></span>
    <span>Video-Platzhalter</span>
  </div>
  {% endif %}
</section>

{% include feature_row %}
