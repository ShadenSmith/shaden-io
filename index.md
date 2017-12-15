---
layout: home
---

I'm a PhD candidate in computer science at the University of Minnesota.  I am
advised by [George Karypis](http://cs.umn.edu/~karypis/) and focus on
developing parallel algorithms for large-scale tensor factorization.  More
broadly, I'm interested in high performance algorithms for large-scale machine
learning and data analytics. Most of my research is released part of
[SPLATT](https://github.com/ShadenSmith/splatt/), an open source software
toolkit for sparse tensor factorization. Another recent project is
[FROSTT](http://frostt.io), a collection of open sparse tensor datasets.

I was at the University of Kentucky from 2009 to 2012 and earned my BSc in
computer science. While there, I did research
under [Mirek Truszczynski](http://cs.uky.edu/~mirek/) and [Brent
Seales](http://www.stoa.org/educe/).

I have completed four internships, most recently at the Intel Parallel
Computing Lab where I developed [high performance algorithms for graph
analytics](http://graphchallenge.mit.edu/champions) and was also involved in
hardware-software codesign.  Before Intel, I spent the summer of 2013 at Lawrence
Livermore National Laboratory (LLNL) porting
[LULESH](https://codesign.llnl.gov/lulesh.php) to OpenACC. The two summers
before LLNL (2011 and 2012), I interned at Lexmark as the developer of a
particle flow modeling engine in CUDA.

## Recent News
<ul>
  {% for post in site.posts %}
    <li>
      {% if post.dest %}
        {{ post.date | date: '%b %d, %Y' }}: <a href="{{ post.dest }}">{{ post.title }}</a>
      {% else %}
          {{ post.date | date: '%b %d, %Y' }}: {{ post.title }}
      {% endif %}
    </li>
  {% endfor %}
</ul>

## Travel
<ul>
	{% assign confs = (site.travel | sort: 'date') | reverse %}
  {% for conf in confs %}
    <li>
      {{ conf.date | date: '%b %d, %Y' }}: <a href="{{ conf.site }}">{{ conf.title }}</a>
          - {{ conf.location }}
    </li>
  {% endfor %}
</ul>


