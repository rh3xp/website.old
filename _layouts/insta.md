---
layout: default
---

    <body>
		<main>
            <div class="posts"> 
              <ul class="links">
                    <h3 class="blog-title">Blog Posts: </h3>
                  {% for post in site.posts %}
                    {% if post.insta %}
                      <li>
                          <a class="post-link" href="{{ post.url }}">{{ post.date | date_to_string }} - {{ post.title }}</a>
                      </li>
                    {% endif %}
                  {% endfor %}
                </ul>
            </div>
        </main>
	</body>

