---
layout: page
title: Fitness Packages
landing-title: "Fitness Packages"
nav-menu: true
description: Crush that training sesh
image: assets/images/fitness_packages_2.jpg
author: null
show_tile: true
---

<!-- Main -->
<div id="main">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h1>Personalised Fitness Packages</h1>
		</header>
		<p>Embarking on a fitness journey is a transformative experience and I'm here to guide you every step of the way. But! I am aware that not everybody is able to afford a PT as it can be quite a costly service.</p>
        <p>Whether you are just starting out on your path to becoming fitter, or are already a fitness powerhouse currently looking to bring extra focus to your training, I offer a range of personalised training packages to cater to your specific requirements like your individual goals, support needs and budget constraints. </p>
        <p>Your fitness journey is unique and your training should definitely reflect that!</p> 
		<p>Let's explore the different options available to ensure you get the right support from me:</p>
	</div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
	{% for package in site.data.packages %}
	<section>
		<div class="image">
			<img src="{% link assets/images/{{ package.image }} %}" alt="" data-position="25% 25%" />
		</div>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h3>{{ package.title }}</h3>
				</header>
				<p>{{ package.content }}</p>
				<button class="button collapsible">Details</button>
				<div class="collapsible-content">
					{% if package.details %}
					<ul class="details">
						{% for item in package.details %}
						<li>{{ item }}</li>
						{% endfor %}
					</ul>
					{% endif %}
					{% if package.enquiry %}
					<p class="price-note">Pricing on Enquiry</p>
					{% elsif package.prices %}
					<h3>Prices</h3>
					{% if package.price_note %}
					<p class="price-note italic">{{ package.price_note }}</p>
					{% endif %}
					<ul class="prices">
						{% for price in package.prices %}
						<li>{{ price }}</li>
						{% endfor %}
					</ul>
					{% endif %}
				</div>
			</div>
		</div>
	</section>
	{% endfor %}
</section>

<!-- Three -->
<section id="three">
	<div class="inner">
		<p>No matter where you are in your fitness journey, I'm committed to helping you achieve your goals. Your success is my priority and I'm dedicated to providing the level of support and affordability that suits your needs. We’ll be in this together!</p>
        <p>I’d love to help transform your life for the better, one step, one workout, and one goal at a time. </p>
        <p>Contact me today to discuss which package aligns with your fitness aspirations and kickstart your journey to the fittest you ever known. ;) </p>
		<ul class="actions">
			<li><a href="#contact" class="button next">Contact Me</a></li>
		</ul>
	</div>
</section>

</div>
