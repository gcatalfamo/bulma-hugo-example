---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
draft: true
---

**Insert Lead paragraph here.****

## New Cool Posts

{{ range first 10 ( where .Site.RegularPages "Type" "posts" ) }}
* {{ .LinkTitle }}
{{ end }}

{{ range first 10 ( where .Site.RegularPages "Type" "posts" ) }}
* {{ .Title }}, {{.ReadingTime}}
 {{.Permalink}}, {{.RelPermalink}}
 {{.Summary}}
{{ end }}

