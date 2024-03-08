---
layout: default
titlecontent: "Blog"
title: "Prochain rendez-vous avec la communauté"

---

{% include nav-head.html %}

<section class="detail_blog">
{% assign current = page.title %}
{% for post in site.data.blog %}
  {% if post.title == current %}
    <article class="post">
      <div class="absolute-bg row" style="background-image: url('{{ site.baseurl }}{{ post.image }}');">
        <!-- Contenu de l'image -->
      </div>
      <div class="post__container">
      <div class="card__footer">
      <div class="user">
        <div class="user__info">
          <h5>{{ post.auteur }}</h5>
          <small>{{ post.date | date: "%b %d, %Y" }}</small>
        </div>
        <img src="{{ site.baseurl }}{{post.img}}" alt="" class="user__image">
      </div>
    </div>
        <span class="post__category">{{ post.category }}</span>
        <div class="post__content">
          <header>
            <h1 class="post__header">{{ post.title }}</h1>
          </header>
          <p class="post__text">{{ post.content | markdownify }}</p>
          <p class="post__text">{{ post.content1 | markdownify }} <a href="{{post.url1}}">{{post.url1}}</a> </p>
          <p class="post__text">{{ post.content2 | markdownify }}</p>
        </div>
        <div class="post__link">
          <div class="col">
            <div class="post-options column-style row">
              <!-- Icônes de partage -->
              <p>Partager</p>
              <div class="col-12">
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
      </div>
    </article>
  {% endif %}
{% endfor %}
</section>





