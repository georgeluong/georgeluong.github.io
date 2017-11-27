---
layout: page
title: Fiction...
excerpt: "A collection of stories and works."
search_omit: false
---
...is a collection of fictional works by me. Though I don't practice the craft nearly enough, I do enjoy writing. The [*Writing Prompts*](https://reddit.com/r/WritingPrompts) subreddit is a great way to challenge myself and exercise my creativity - I suspect most of the posts that end up here will be responses to prompts from there.

When inspiration *does* strike, the finished products will be added here.

<ul class="post-list">
{% for post in site.categories.fiction %}
  <li><article><a href="{{ site.url }}{{ post.url }}">{{ post.title }} <span class="entry-date"><time datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%B %d, %Y" }}</time></span>{% if post.excerpt %} <span class="excerpt">{{ post.excerpt | remove: '\[ ... \]' | remove: '\( ... \)' | markdownify | strip_html | strip_newlines | escape_once }}</span>{% endif %}</a></article></li>
{% endfor %}
</ul>

<script>
  (function (w,i,d,g,e,t,s) {w[d] = w[d]||[];t= i.createElement(g);
    t.async=1;t.src=e;s=i.getElementsByTagName(g)[0];s.parentNode.insertBefore(t, s);
  })(window, document, '_gscq','script','//widgets.getsitecontrol.com/114371/script.js');
</script>
