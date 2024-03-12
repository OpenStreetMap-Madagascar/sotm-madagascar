---
layout: default
titlecontent: "Blog"
title: "Prochain rendez-vous avec la communauté"

---

{% include nav-head.html %}

<section class="detail_blog">
  <div class="container">
{% assign current = page.title %}
{% for post in site.data.blog %}
  {% if post.title == current %}
  <div class="footer-contact mt-40">
                              <h5 class="f-title">Partager le blog</h5>
                              <ul class="social">
                                  <li><a class=" wow fadeInUp" data-wow-duration="1s" target="_blank" href="https://api.whatsapp.com/send?text={{ site.baseurl }}{{ post.url }}"><i class="lni lni-whatsapp"></i></a></li>
                                  <li><a class=" wow fadeInUp" data-wow-duration="1s" target="_blank" href="https://www.linkedin.com/shareArticle?url={{ site.baseurl }}{{ post.url }}"><i class="lni lni-linkedin"></i></a></li>
                                  <li><a class=" wow fadeInUp" data-wow-duration="1.5s" href="https://twitter.com/intent/tweet?url={{ site.baseurl }}{{ post.url }}"><i class="lni lni-twitter"></i></a></li>
                                  <li><a class=" wow fadeInUp" data-wow-duration="2s" href="https://www.facebook.com/sharer/sharer.php?u={{ site.baseurl }}{{ post.url }}"><i class="lni lni-facebook"></i></a></li>
                              </ul>
                          </div>
    <article class="post">
      <div class="absolute-bg row" style="background-image: url('{{ site.baseurl }}{{ post.image }}');">
        <!-- Contenu de l'image -->
      </div>
      <div class="post__container">
      <div class="">
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
      </div>
    </article>
  {% endif %}
{% endfor %}
</div>
</section>





