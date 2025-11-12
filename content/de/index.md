---
title: "Projekte"
layout: "projects"
---

Hier findest du eine Übersicht der Projekte.

{{ range .RegularPages.ByDate.Reverse }}
  <article class="project-card">
    {{ with .Params.image }}
      <a href="{{ $.RelPermalink }}">
        <img src="{{ . | relURL }}" alt="{{ $.Title }}" class="project-thumb">
      </a>
    {{ end }}
    <h2><a href="{{ .RelPermalink }}">{{ .Title }}</a></h2>
    {{ if .Date }}<small>{{ .Date.Format "2006" }}</small>{{ end }}
    <p>{{ .Summary }}</p>
  </article>
{{ end }}
