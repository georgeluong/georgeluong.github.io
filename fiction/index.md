---
layout: page
title: Fiction...
excerpt: "An archive of stories/works by George, sorted by date."
search_omit: true
---
...is a collection of fictional works by me. Though I don't practice the craft enough, I do enjoy writing. I find that the [*WritingPrompts* subreddit](https://reddit.com/r/WritingPrompts) is a great way to challenge myself and exercise my creative muscles - I suspect most of the posts that end up here will be responses to prompts from there.

When inspiration strikes, the finished products will be added here.

# Latest

<ul class="post-list">
{% for post in site.categories.fiction %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>
