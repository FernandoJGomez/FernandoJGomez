---
title: "Teaching"
layout: textlay
excerpt: "Fernando J. Gomez -- Teaching"
sitemap: false
permalink: /teaching/
---

# Teaching

##  2010 - 2021

_“Learning is never cumulative, it is a movement of knowing which has no beginning and no end.” (Bruce Lee)_

{% assign number_printed = 0 %}
{% for publi in site.data.classlist %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if publi.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<style>
        .well {
            background-color: rgb(209, 242, 215);
        }
    </style>
    
<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ publi.title }}</pubtit>

  <img src="{{ site.url }}{{ site.baseurl }}/images/classpic/{{ publi.image }}" class="img-responsive" width="50%" style="float: right" />
  
  <p>{{ publi.description }}</p><br>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p>{{ publi.authors }} {{ publi.year }}
   <em><a href="{{ publi.link.url }}">{{ publi.link.display }} {{ publi.doi }}</a></em></p>
  
  <p> *{{ publi.news2 }}*</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>

