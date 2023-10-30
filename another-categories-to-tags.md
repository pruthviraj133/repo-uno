
<div class="tags-expo">
  <div class="tags-expo-list">
    {% for tag in site.tags %}
    <font size='+2'>#<a href="#{{ tag[0] | slugify }}" class="post-tag">{{ tag[0] }}</a></font>
    {% endfor %}
  </div>
  <hr/>
  <div class="tags-expo-section">
    {% for tag in site.tags %}
    <h2 id="{{ tag[0] | slugify }}">#{{ tag | first }}</h2>
    <ul class="tags-expo-posts">
      {% for post in tag[1] %}
      <li><a class="post-title" href="{{ site.baseurl }}{{ post.url }}">{{post.title}}</a> | <small>{{ post.date | date_to_string }}</small></li>
      {% endfor %}
    </ul>
    {% endfor %}
  </div>
</div>