---
layout: page
title: Classes
landing-title: "Classes"
nav-menu: true
description: Bring your friends too
image: assets/images/classes.jpeg
author: null
show_tile: true
---

<div id="main">
    <section id="one">
        <div class="inner">
            <header class="major">
                <h1>Classes</h1>
            </header>
            <div class="split-header">
                <p class="text-body">Enjoy training, but prefer the energy of group workouts? <br /><br />
                Love dancing, but find yourself unsure of your moves around others? <br /><br />
                Check out my Fitness and Dance classes below! Whether you're seeking quick sweaty sessions, aiming to learn how to lift, or eager to get some dance steps up your sleeve, I've got you covered. <br /><br />
                Ready to join the fun?</p>
                <div class="image">
                    <img src="{% link assets/images/classes_header.jpeg %}" alt="" data-position="25% 25%" />
                </div>
            </div>
        </div>
    </section>
    <section id="two">
        <div class="inner">
            <h2>Fitness Classes</h2>
            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th>Class</th>
                            <th>Location</th>
                            <th>Day</th>
                            <th>Time</th>
                            <th>Details</th>
                        </tr>
                    </thead>
                    <tbody>
                        {% for class in site.data.fitness_classes %}
                        <tr>
                            <td>{{ class.name }}</td>
                            <td>{{ class.location }}</td>
                            <td>{{ class.day }}</td>
                            <td>{{ class.time }}</td>
                            <td><a href="{{ class.url }}">See here</a></td>
                        </tr>
                        {% endfor %}
                    </tbody>
                </table>
            </div>
        </div>
    </section>
    <section id="three">
        <div class="inner">
            <h2>Dance Classes</h2>
            <div class="table-wrapper">
                <table>
                    <thead>
                        <tr>
                            <th>Class</th>
                            <th>Location</th>
                            <th>Day</th>
                            <th>Time</th>
                            <th>Details</th>
                        </tr>
                    </thead>
                    <tbody>
                        {% for class in site.data.dance_classes %}
                        <tr>
                            <td>{{ class.name }}</td>
                            <td>{{ class.location }}</td>
                            <td>{{ class.day }}</td>
                            <td>{{ class.time }}</td>
                            <td><a href="{{ class.url }}">See here</a></td>
                        </tr>
                        {% endfor %}
                    </tbody>
                </table>
            </div>
        </div>
    </section>
</div>