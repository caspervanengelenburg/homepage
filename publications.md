---
layout: default
title: "Research"
permalink: /research/
---

<h1 id="research"></h1>

<h2 style="margin: 60px 0px -15px;">Research</h2>
<br>

The research I conduct is in most cases a mix of (graph) machine learning, computer vision, and architectural design & data representation. 
My focus is on <strong>floor plan representation learning</strong>. 
I have only added a few of my publications here: the ones that are most dear to me.
As a matter of facts, most of the papers that I am an author of are <em>not</em> listed below.
For a complete overview, have a look at [my Google Scholar account](https://scholar.google.com/citations?user=6QHnxs8kMSwC&hl=en).


### Highlights

<div class="publications">
<ol class="bibliography">

{% assign highlights = site.data.publications.main
  | where_exp: "p","p.featured"
  | sort: "year" | reverse %}

{% for link in highlights %}

<li>
<div class="pub-row">
  <div class="col-sm-3 abbr" style="position: relative;padding-right: 15px;padding-left: 15px;">
    <img src="{{ link.image }}" class="teaser img-fluid z-depth-1" style="width=100;height=40%">
            <abbr class="badge">{{ link.conference_short }}</abbr>
  </div>
  <div class="col-sm-9" style="position: relative;padding-right: 15px;padding-left: 20px;">
      <div class="title"><a href="{{ link.pdf }}">{{ link.title }}</a></div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>
      </div>
    <div class="links">
      {% if link.pdf %} 
      <a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">PDF</a>
      {% endif %}
      {% if link.code %} 
      <a href="{{ link.code }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Code</a>
      {% endif %}
      {% if link.page %} 
      <a href="{{ link.page }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Project Page</a>
      {% endif %}
      {% if link.data %} 
      <a href="{{ link.data }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">Dataset</a>
      {% endif %}
      {% if link.bibtex %} 
      <a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" role="button" target="_blank" style="font-size:12px;">BibTex</a>
      {% endif %}
      {% if link.notes %} 
      <strong> <i style="color:#e74d3c; font-weight:600">{{ link.notes }}</i></strong>
      {% endif %}
      {% if link.others %} 
      {{ link.others }}
      {% endif %}
    </div>
  </div>
</div>
</li>

<br>

{% endfor %}

</ol>
</div>

<!--
### Other publications
<ol class="bibliography plain">
{% assign remaining = site.data.publications.main
  | where_exp: "p","p.featured != true"
  | sort: "year" | reverse %}
{% for link in remaining %}
<li>
  <div class="pub-row">
    <div class="col-sm-12" style="position: relative;padding-right: 15px;padding-left: 15px;">
      <div class="title">
        {% if link.pdf %}<a href="{{ link.pdf }}">{% endif %}{{ link.title }}{% if link.pdf %}</a>{% endif %}
      </div>
      <div class="author">{{ link.authors }}</div>
      <div class="periodical"><em>{{ link.conference }}</em>{% if link.year %} {{ link.year }}{% endif %}</div>
      <div class="links">
        {% if link.pdf %}<a href="{{ link.pdf }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">PDF</a>{% endif %}
        {% if link.code %}<a href="{{ link.code }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Code</a>{% endif %}
        {% if link.page %}<a href="{{ link.page }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Project Page</a>{% endif %}
        {% if link.data %}<a href="{{ link.data }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">Dataset</a>{% endif %}
        {% if link.bibtex %}<a href="{{ link.bibtex }}" class="btn btn-sm z-depth-0" target="_blank" style="font-size:12px;">BibTex</a>{% endif %}
        {% if link.notes %}<strong><i style="color:#e74d3c; font-weight:600">{{ link.notes }}</i></strong>{% endif %}
        {% if link.others %}{{ link.others }}{% endif %}
      </div>
    </div>
  </div>
</li>
<br>
{% endfor %}
</ol>
-->
