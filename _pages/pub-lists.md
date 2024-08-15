---
permalink: /publications/lists
title: "Publication Lists"
---

My Lists: [Sorted by Year](/publications/pubsbyyear), [Sorted by Type](/publications/pubsbytype)

{% if page.author and site.data.authors[page.author] %}
  {% assign author = site.data.authors[page.author] %}{% else %}{% assign author = site.author %}
{% endif %}

External Lists:
* [Google Scholar]({{ author.googlescholar }})
* [Researchgate]({{ author.researchgate }})
* [ORCID]({{ author.orcid }})
* [Scopus]({{ author.scopus }})
* [Web of Science]({{ author.wos }})
