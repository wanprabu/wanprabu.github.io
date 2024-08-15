---
permalink: /publications/lists
title: "Publication Lists"
---

My Lists: [Sorted by Year](/publications/pubsbyyear), [Sorted by Type](/publications/pubsbytype)

{% if page.author and site.data.authors[page.author] %}
  {% assign author = site.data.authors[page.author] %}{% else %}{% assign author = site.author %}
{% endif %}

External Lists:
* Google Scholar {{ author.googlescholar }}
* [Researchgate]{{ author.researchgate }}
* [ORCID]({{ author.orcid }})
* [Scopus](http://www.scopus.com/authid/detail.url?authorId=57188879511)
* [Web of Science](https://www.webofscience.com/wos/author/record/JBS-4174-2023)
