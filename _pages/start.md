---
layout: splash
permalink: /
hidden: true
header:
  overlay_color: "#003594"
  overlay_image: /assets/images/mm-home-page-feature.jpg
  show_overlay_excerpt: false
video_path: /assets/videos/intro.mp4
excerpt: >
  Das Zentrum für Robotik an der Hochschule Heilbronn ist eine interdisziplinäre Einrichtung, die sich der Forschung, Lehre und praxisnahen Entwicklung innovativer Lösungen im Bereich der Robotik widmet. <br />
  Im Fokus stehen moderne Technologien wie kollaborierende Robotersysteme (Cobots), künstliche Intelligenz in der Robotik sowie die klassische Industrierobotik. Studierende erhalten die Möglichkeit, in modernen Laboren praxisnahe Erfahrungen zu sammeln und an aktuellen Forschungsprojekten mitzuwirken – von der Konzeption über die Programmierung bis hin zur Umsetzung realer Anwendungen.
feature_row:
  - image_path: /assets/images/mm-customizable-feature.png
    alt: "customizable"
    title: "Super customizable"
    excerpt: "Everything from the menus, sidebars, comments, and more can be configured or set with YAML Front Matter."
    url: "/docs/configuration/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - image_path: /assets/images/mm-responsive-feature.png
    alt: "fully responsive"
    title: "Responsive layouts"
    excerpt: "Built with HTML5 + CSS3. All layouts are fully responsive with helpers to augment your content."
    url: "/docs/layouts/"
    btn_class: "btn--primary"
    btn_label: "Learn more"
  - image_path: /assets/images/mm-free-feature.png
    alt: "100% free"
    title: "100% free"
    excerpt: "Free to use however you want under the MIT License. Clone it, fork it, customize it... whatever!"
    url: "/docs/license/"
    btn_class: "btn--primary"
    btn_label: "Learn more"      
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
