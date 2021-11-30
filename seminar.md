---
layout: default
---

<div class="posts">
  {% assign sorted = site.seminars | sort: 'date' | reverse %}
  {% for post in sorted %}
    <article class="post">

      <div class="titles">
	<br/>
        <b>
	Time: {{ post.date | date: "%b %d (%a)"}}
	@ {{ post.time }},
        Location: {{ post.location }}
        {% if post.location %} {% if post.online %} and {% endif %}{% endif %}
        {% if post.online %} online {% endif %}
        </b>
        <br/>
	{{ post.speaker }} ({{ post.affiliation }}),
	"{{ post.talk-title }}"
      </div>
      <a href="{{ site.baseurl }}{{ post.url }}" class="read-more">Abstract and bio</a>
    </article>
  {% endfor %}
</div>
