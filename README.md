## Updating Sections

Here are a few how-tos for some of the most likely areas you're going to want to add to/change :)

### General

- All images are stored in `assets/images`

### Challenges

- Each challenge has its own page, stored in [_posts](./_posts/)
- A challenge file must have the `.md` extension, and begin with the following details:
```yaml
---
layout: challenge
title: $TITLE
description: "$DESCRIPTION"
image: $PICTURE.jpg
---
```
- After that fill the file with whatever contents you like (probably easiest to copy an existing challenge and go from there).
- The post main contents obeys **markdown** formatting

### Recipes

- Recipes are stored in `_data/recipes.yaml`:
- They must have the following format:
```yaml
- title: $TITLE
  category: $CATEGOry
  prep_time: X mins
  serves: 1
  image: $IMAGE.jpeg
  ingredients:
      - Item 1
      - Item 2
      - ...
  optional_ingredients:
      - Item 1
      - Item 2
      - ...
  description: |
    Main contents...
```
- Description obeys **markdown** formatting

### Fitness Packages

- Packages are stored in `_data/packages.yaml`:
- They must have the following format:
```yaml
- title: $TITLE
  image: $IMAGE.jpg
  content: |
    Long description...
  details: 
      - Item 1
      - Item 2
      - ...
  prices:
      - Item 1
      - Item 2
      - ...
```
- Description obeys **plain text** formatting

### Classes


- Dance classes are stored in `_data/dance_classes.yaml`:
- Fitness classes are stored in `_data/fitness_classes.yaml`:
- They must have the following format:
```yaml
- name: $NAME
  location: $LOCATION
  day: Monday-Sunday
  time: "19:30"
  url: https://$LINK
```

---

# Credits

## Forty Theme

Based on the [Forty Jekyll Theme](https://github.com/andrewbanchich/forty-jekyll-theme).

Original README from HTML5 UP:

```
Forty by HTML5 UP
html5up.net | @ajlkn
Free for personal and commercial use under the CCA 3.0 license (html5up.net/license)


This is Forty, my latest and greatest addition to HTML5 UP and, per its incredibly
creative name, my 40th (woohoo)! It's built around a grid of "image tiles" that are
set up to smoothly transition to secondary landing pages (for which a separate page
template is provided), and includes a number of neat effects (check out the menu!),
extra features, and all the usual stuff you'd expect. Hope you dig it!

Demo images* courtesy of Unsplash, a radtastic collection of CC0 (public domain) images
you can use for pretty much whatever.

(* = not included)

AJ
aj@lkn.io | @ajlkn


Credits:

	Demo Images:
		Unsplash (unsplash.com)

	Icons:
		Font Awesome (fortawesome.github.com/Font-Awesome)

	Other:
		jQuery (jquery.com)
		html5shiv.js (@afarkas @jdalton @jon_neal @rem)
		background-size polyfill (github.com/louisremi)
		Misc. Sass functions (@HugoGiraudel)
		Respond.js (j.mp/respondjs)
		Skel (skel.io)
```

Repository [Jekyll logo](https://github.com/jekyll/brand) icon licensed under a [Creative Commons Attribution 4.0 International License](http://choosealicense.com/licenses/cc-by-4.0/).
