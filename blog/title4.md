---
layout: default
titlecontent: "Blog"
title: "What's new in 2022 Tech4"

---

{% include nav-head.html %}

<section class="detail_blog">
{% assign current = page.title %}
{{ current }}

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
      <div class="absolute-bg row" style="background-image: url('{{ post.image }}');">
        <!-- Contenu de l'image -->
      </div>
      
      <div class="post__container">
        <span class="post__category">{{ post.category }}</span>
        
        <div class="post__content">
          <header>
            <time class="post__time">{{ post.date | date: "%b %d, %Y" }}</time>
            <h1 class="post__header">{{ post.title }}</h1>
          </header>
          
          <p class="post__text">{{ post.content | markdownify }}</p>
        </div>
        
        <div class="post__link">
          <div class="col">
            <div class="post-options column-style row">
              <!-- Icônes de partage -->
              <p>Partager</p>
              <div class="col-12">
               <a href="https://api.whatsapp.com/send?text={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/whatsapp.png" alt="WhatsApp">
                </a>
                <a href="https://www.facebook.com/sharer/sharer.php?u={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/facebook.png" alt="Facebook">
                </a>
                <a href="https://twitter.com/intent/tweet?url={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/twintter.png" alt="Twitter">
                </a>
                <a href="https://www.linkedin.com/shareArticle?url={{ site.baseurl }}{{ post.url }}" target="_blank" class="share-icon">
                  <img src="/assets/images/icons/linkedin.png" alt="LinkedIn">
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