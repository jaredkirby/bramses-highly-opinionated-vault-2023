If you use Readwise, you'll be able to have resources auto sync from Kindle + the web. They'll end up in the  `/Readwise` directory.

## Dataview Test (should have one item)
```dataview
list from "Readwise" 
where project = "Test Project"
```

## Page Metadata Formatting

```
---
author: {% if author %}{{author}}{% endif %}
fullTitle: {{full_title}}
category: #{{category}}
source: {{source}}
date: [[{{date}}]]
time: {{time}}
{% if image_url -%}
imageURL: {{image_url}}
{% endif -%}
{% if book_id -%}
bookID: {{book_id}}
{% endif -%}
{% if document_tags -%}
documentTags: {% for tag in document_tags %}#{{tag}} {% endfor %}
{% endif -%}
{% if url -%}
url: {{url}}
{% endif -%}
project: -
---
```


## Highlights Header Formatting

```
{% if is_new_page %}
## Highlights
{% elif has_new_highlights -%}
## New highlights added {{date|date('F j, Y')}} at {{time}}
{% endif -%}
```


## Highlight Formatting

```
---

> {{ highlight_text }}{% if highlight_location and highlight_location_url %} ([{{highlight_location}}]({{highlight_location_url}})){% elif highlight_location %} ({{highlight_location}}){% endif %}{% if highlight_tags %}
    - Tags: {% for tag in highlight_tags %} #{{tag}} {% endfor %}{% endif %}{% if highlight_note %}
    - Note: {{ highlight_note }}{% endif %}

---
```


## Sync Notification
```
- [[{{date|date('Y-m-d')}}]] {{time}} — Synced {{num_highlights}} highlight{{num_highlights|pluralize}} from {{num_books}} document{{num_books|pluralize}}.
{% for book in books %}    - {{ book.num_highlights_added}} highlights from {{ book.title }}
{% endfor %}
```