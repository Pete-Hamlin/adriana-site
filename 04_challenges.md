---
layout: page
title: Challenges
landing-title: "Challenges"
nav-menu: true
description: Push yourself
image: assets/images/challenges.jpeg
author: null
show_tile: true
---
<div id="main">
    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>Challenges</h1>
            </header>
            <p>Being active doesn't have to be all hard work, and it doesn't have to take hours of your day either!<br /><br />
            Here I’ll be posting some fun challenges to help you keep your training interesting & exciting. They will be pretty varied - ‘cause I don’t know what I would do without A LOT of variety in my workouts - so you may find some pretty easy & some may give you a good run for your money! I’ll keep them home-friendly & equipment-free so you can do them anywhere, anytime.<br /><br />
            Show your competitive side and challenge your friends, or just prove to yourself what you're capable of. If you complete one of my challenges, I'd love to hear about it!
            </p>
        </div>
    </section>
    <section id="two" class="spotlights">
        {% for post in site.posts %}
            {% if post.title != 404 and post.layout == "challenge" %}
                <section>
                    {% if post.image %}
                    <div class="image"><img src="{% link assets/images/{{ post.image }} %}" alt="" /></div>
                    {% endif %}
                    <div class="content">
                    <div class="inner">
                        <header class="minor">
                            <h1><a href="{{ post.url }}">{{ post.title }}</a></h1>
                        </header>
                        <span class="subheading">
                            {% if post.date %}
                            <p class="post-date italic">{{ post.date }}</p>
                            {% endif %}
                            <span class="post-info">
                                {% if post.workout_length %}
                                <p>Workout Length: {{ post.workout_length }}</p>
                                {% endif %}
                            </span>
                        </span>
                        <p>{{ post.content | strip_html | truncate: 200 }}</p>
                    </div>
                    </div>
                </section>
            {% endif %}
        {% endfor %}
    </section>
</div>
