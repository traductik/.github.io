---
layout: page
title:  "Articles & actualités stylistiques"
breadcrumb: "Articles & actualités stylistiques"
permalink: /blog_fr/technique/stylistique/
date: 2017-11-28
nav: nosideblog
category: stylistic
ref: stylistiquewelcome
lang: fr
---


<!----------------- Liste des articles de blog ------------------->
  <div class="wrapper">
  <h1 class="page-heading">Articles dans la catégorie</h1>
 <ul class="post-list">
	{% assign posts=site.posts | where:"lang", page.lang %}
    {% assign catposts=posts | where:"category", page.category %}
    {% for catpost in catposts %}
      <li>
        <span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>

        <h2>
          <a class="post-link" style="font-size:60%" href="{{ catpost.url | prepend: site.baseurl }}">{{ catpost.title }}</a>
        </h2>
      </li>
    {% endfor %}
  </ul>
  </div>
  <!----------------- Fin de la liste des articles de blog ------------------->
