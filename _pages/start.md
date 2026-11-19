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
    excerpt: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet."
  - image_path: /assets/images/embodied_ai.jpg
    alt: "embodied AI"
    title: |
      Embodied AI
    excerpt: "Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet."  
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

<section class="home-topics" aria-label="Forschungsthemen">
  {% include feature_row %}
</section>
