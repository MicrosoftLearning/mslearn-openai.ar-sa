---
title: تمارين Azure OpenAI
permalink: index.html
layout: home
---

# تمارين Azure OpenAI

صُممِّت التمارين التالية لدعم الوحدات النمطية على [Microsoft Learn](https://learn.microsoft.com/training/browse/?terms=OpenAI).


{% assign labs = site.pages | where_exp:"page", "page.url contains '/Instructions/Exercises'" %} {% for activity in labs  %}
- [{{ activity.lab.title }}]({{ site.github.url }}{{ activity.url }}) {% endfor %}
