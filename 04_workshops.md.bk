---
layout: page
title: Workshops
landing-title: "Workshops"
nav-menu: true
description: Specialist Workshops
image: assets/images/workshops.jpg
author: null
show_tile: true
---
<div id="main">
    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>Workshops</h1>
            </header>
        </div>
    </section>
    <section id="two" class="spotlights">
        {% for workshop in site.data.workshops %}
        <section>
            {% if workshop.image %}
            <a href="{{ post.url }}" class="image"><div class="image"><img src="{% link assets/images/{{ workshop.image }} %}" alt="" /></div></a>
            {% endif %}
            <div class="content">
                <div class="inner">
                    <header class="minor">
                        <h1>{{ workshop.title }}</h1>
                    </header>
                    <span class="subheading">
                        <span class="post-info">
                            {% if workshop.date %}
                            <span>{{ workshop.date }} - {{ workshop.location }}</span>
                            {% endif %}
                        </span>
                    </span>
                    <h3>£{{ workshop.price }}</h3>
                    <!-- <p>{{ workshop.description }}</p> -->
                    <ul class="details">
                        {% for item in workshop.details %}
                        <li>{{ item }}</li>
                        {% endfor %}
                    </ul>
                    <ul class="actions">
                        <li><a href="{{ workshop.link }}" class="button next" target="_blank">Book Now!</a></li>
                    </ul>
                </div>
            </div>
        </section>
        {% endfor %}
    </section>
</div>
