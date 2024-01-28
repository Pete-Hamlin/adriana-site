---
layout: page
title: Foodspiration
landing-title: "Foodspiration"
nav-menu: true
description: Fuel your body
image: assets/images/fruity_oats.jpeg
author: null
show_tile: true
category: food
---
<div id="main">
    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>Foodspiration</h1>
            </header>
            <p>I love food. Food is life. Food is fuel for my body that enables it to do all the stuff I want it to do.</p>
            <p>But I don’t really have any time to spend cooking, so I have become really good at eating healthy with minimal time spent in the kitchen. </p>
            <p>I will be sharing my food secrets with you on here in the hope that it helps improve your eating habits without hassle. Be warned though! You will have to start eating your veggies hehe ^_^</p>
        </div>
    </section>
    <section id="two" class="spotlights">
        {% for recipe in site.data.recipes %}
                <section>
                    {% if recipe.image %}
                    <div class="image"><img class="recipe" src="{% link assets/images/{{ recipe.image }} %}" alt="" /></div>
                    {% endif %}
                    <div class="content">
                        <div class="inner">
                            <header class="minor">
                                <h1 class="recipe">{{ recipe.title }}</h1>
                                <h4>{{ recipe.category }}</h4>
                            </header>
                            <span class="subheading">
                                <p class="recipe-serves italic">Serves: {% if recipe.serves %}{{recipe.serves}}{% else %}1{% endif %}</p>
                                <span class="recipe-prep">
                                    <p>Preparation time:{% if recipe.prep_time %} {{ recipe.prep_time }}{% else %}5 mins{% endif %}</p>
                                </span>
                            </span>
                            <span class="recipe-content">
                                {% if recipe.ingredients %}
                                <div>
                                    <h4>Ingredients</h4>
                                    <ul>
                                    {% for ingredient in recipe.ingredients %}
                                        <li>{{ ingredient }}</li>
                                    {% endfor %}
                                    </ul>
                                </div>
                                {% endif %}
                                {% if recipe.optional_ingredients %}
                                <div>
                                    <h4>Optional Extras</h4>
                                    <ul>
                                    {% for ingredient in recipe.optional_ingredients %}
                                        <li>{{ ingredient }}</li>
                                    {% endfor %}
                                    </ul>
                                </div>
                                {% endif %}
                                {% if recipe.description %}
                                <div>
                                    <span>{{ recipe.description | markdownify }}</span>
                                </div>
                                {% endif %}
                            </span>
                        </div>
                    </div>
                </section>
        {% endfor %}
    </section>
</div>
