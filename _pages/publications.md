---
title: "Fernando J. Gomez - Publications"
layout: gridlay
excerpt: "Fernando J. Gomez -- Publications"
sitemap: false
permalink: /publications/
---


# Publications (under construction yet, for updated list wee CV)

Jump to the bottom of the page to see a [full list of publications](#full-list) and [Preprints](#preprints). A complete list of papers and conference abstracts is also available in my [Google Scholar](https://scholar.google.com/citations?user=3pa76GEAAAAJ&hl=en&oi=ao) profile.

## Highlights

{% assign number_printed = 0 %}
{% for publi in site.data.publist %}

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
  <img src="{{ site.url }}{{ site.baseurl }}/images/pubpic/{{ publi.image }}" class="img-responsive" width="50%" style="float: left" />
  <p>{{ publi.description }}</p>
  <p>{{ publi.authors }}. {{ publi.year }}. {{ publi.title }}. <em><a href="{{ publi.link.url }}">{{ publi.link.display }}. {{ publi.doi }}</a></em></p>
  <p class="text-danger"><strong> {{ publi.news1 }}</strong></p>
  <p> {{ publi.news2 }}</p>
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


## Full List

{% for publi in site.data.publist %}

  {{ publi.authors }}. <strong>{{ publi.year }}</strong>. {{ publi.title }}. <em><a href="{{ publi.link.url }}">{{ publi.link.display }}. {{ publi.doi }}</a></em>

{% endfor %}

## Preprints
{% for publi in site.data.preprintlist %}

  {{ publi.authors }}. <strong>{{ publi.year }}</strong>. {{ publi.title }}. <em>{{ publi.link.display }}</em>

{% endfor %}
