---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

## Education
<ul>
	<li>
		<span class="text-info"><b>Ph.D in Computer Science (Machine Learning)</b></span>, Aarhus University, 2021 (expected)
	</li>
	<li>
		<span class="text-info"><b>M.S. in Computer Science</b></span>, Aarhus University, 2018.<br/>
    	<b>Specialization</b>: Algorithms and Machine Learning.<br/>
    	<b>Thesis</b>: <i>Explainable Deep Learning: Facilitating the Use of Deep Neural Networks in Healthcare, grade: 12</i>.<br/>
    	<b>Weighted GPA</b>: 10.4 on a 12 scale<br/>
    	<b>Courses from other universities</b>: Advanced Machine Learning (DTU, grade: 12), Computational Data Analysis (DTU, 12), Algorithms for Massive Data Sets (DTU, 12), Introduction to Artificial Intelligence (UC Berkeley, A), Introductory Applied Econometrics (UC Berkeley, A).
	</li>
	<li>
		<span class="text-info"><b>B.S. in Computer Science</b></span>, Aarhus University, 2015.<br/>
    	<b>GPA</b>: 8.91 on a 12 scale.<br/>
    	<b>Bachelor thesis</b>: <i>Compiler for the programming language Tiger, Grade: 12</i>.
	</li>
</ul>
  
## Teaching
  <ul>
	{% for post in site.teaching reversed %}
		<div class="{{ include.type | default: "list" }}__item">
  	  	  <article class="archive__item" itemscope itemtype="http://schema.org/CreativeWork">
    		<li>
    		<h3 class="archive__item-title" itemprop="headline">
      	  	  {% if post.link %}
        		<a href="{{ post.link }}">{{ post.title }}</a> <a href="{{ base_path }}{{ post.url }}" rel="permalink"><i class="fa fa-link" aria-hidden="true" title="permalink"></i><span class="sr-only">Permalink</span></a>
      	  	  {% else %}
        		<a href="{{ base_path }}{{ post.url }}" rel="permalink">{{ post.title }}</a>
      	  	  {% endif %}
    		</h3>
    		{% if post.date %}<p class="page__meta"><i class="fa fa-clock-o" aria-hidden="true"></i> {{ post.date | date: '%B %d, %Y' }}</p>{% endif %}
    		{% if post.venue%}<p class="archive__item-excerpt" itemprop="description">{{post.type}} at {{ post.venue }},  {{post.location}}</p>{% endif %}
    		</li>
  	  	  </article>
		</div>
	{% endfor %}
</ul>

## Work experience
* <span class="text-info">2015-2016</span> Windows (WPF) Developer at Visiolink ApS, Aarhus, Denmark. 
* <span class="text-info">2013-2015</span> Student Developer at Visiolink ApS, Aarhus, Denmark

## Talks
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html %}
  {% endfor %}</ul>

## Skills
* Python
  * Tensorflow
  * Pytorch
  * Keras
  * Numpy
* MatLab
* R
* Java
* C++
  
## Portfolio
<ul>
	<li>Automatic Layer-wise Relevance Propagation (LRP) framework for Tensorflow 1.4 available on <a href="https://github.com/fhvilshoj/lrp">GitHub</a>.</li>
	<li>Expectation Maximization for Kalman Filters <a href="https://github.com/fhvilshoj/greensteam">GitHub</a>.</li>
	<li>Material from study group on GANs <a href="https://github.com/fhvilshoj/GANs">GitHub</a>.</li>
</ul>

## Service and leadership
* <span class="text-info">2016-2017</span> Board member of the Computer Science student organization ([DSAU](https://dsau.dk/)) as Aarhus University.
* Endless hours of gymnastics teaching.
