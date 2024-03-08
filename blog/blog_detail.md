---
layout: default
titlecontent: "Blog"
title: "SOTM 2019 Heidelberg"

---
{% include nav-head.html %}
<section class="detail_blog">
{% assign current = page.title %}
{% for post in site.data.blog %}
  {% if post.title == current %}
    <article class="post">
      <div class="absolute-bg row" style="background-image: url('{{ post.image }}');">
        <!-- Contenu de l'image -->
      </div>
      <div class="post__container">
      <div class="card__footer">
      <div class="user">
        <div class="user__info">
          <h5>{{ post.auteur }}</h5>
          <small>{{ post.date | date: "%b %d, %Y" }}</small>
        </div>
        <img src="{{post.img}}" alt="" class="user__image">
      </div>
    </div>
        <span class="post__category">{{ post.category }}</span>
    <div class="post__content">
      <header>
        <h1 class="post__header">{{ post.title }}</h1>
      </header>
      <p class="post__text">{{ post.content | markdownify }}</p>
      <p class="post__text">{{ post.content1 | markdownify }}</p>
    </div>
  </div>
</article>
<article class="post">
  <div class="absolute-bg row" style="background-image: url('{{ post.image2 }}');">
  </div>
  <div class="post__container">
  <div class="post__content">
    <span class="post__time">{{ post.soustitre }}</span>
    <p class="post__text">{{ post.content2 | markdownify }}</p>
    <span class="post__time">{{ post.soustitre1 }}</span>
    <p class="post__text">{{ post.content3 | markdownify }}</p>
    <div class="list">
  <p>{{post.liste1}}<a href="https://github.com/jenningsanderson/aws-athena-workshop">here</a></p>
  <p>{{post.liste2}}<a href="https://docs.google.com/presentation/d/1GTfi0BhHyOxydnb04G69eTuQRqJswn6eHbHpyrT250U/edit?pli=1#slide=id.g603ddb3b17_0_1477">Slide</a></p>
  <p>{{post.liste3}}<a href="https://media.ccc.de/v/sotm2019-1332-spatial-indexes-for-osm-in-postgis">here</a></p>
  <p>{{post.liste4}}<a href="https://media.ccc.de/v/sotm2019-at-1905-bridging-the-map-exploring-interactions-between-the-academic-and-mapping-communities-in-openstreetmap">here</a></p>
  <p>{{post.liste5}}<a href="https://media.ccc.de/v/sotm2019-1235-share-edits-and-insights-with-the-overpass-tools">here</a></p>
</div>
    <p class="post__text">{{ post.content4 | markdownify }}</p>
    </div>
  </div>
</article>    
    <div class="post__link">
          <div class="col">
            <div class="post-options column-style row">
              <div class="col-12">
                <div class="post__time">Partager</div>
                <a href="https://www.facebook.com/sharer/sharer.php?u={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/facebook.png" alt="Facebook">
                </a>
                <a href="https://twitter.com/intent/tweet?url={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/twintter.png" alt="Twitter">
                </a>
                <a href="https://www.linkedin.com/shareArticle?url={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/linkedin.png" alt="LinkedIn">
                </a>
                <a href="https://api.whatsapp.com/send?text={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/whatsapp.png" alt="WhatsApp">
                </a>
                <!-- Ajoutez d'autres icônes au besoin -->
              </div>
            </div>
          </div>
        </div>
  {% endif %}
{% endfor %}
</section>