<p align="center">
  <a href="https://revealjs.com">
  <img src="https://hakim-static.s3.amazonaws.com/reveal-js/logo/v1/reveal-black-text-sticker.png" alt="reveal.js" width="500">
  </a>
  <br><br>
  <a href="https://github.com/hakimel/reveal.js/actions"><img src="https://github.com/hakimel/reveal.js/workflows/tests/badge.svg"></a>
  <a href="https://slides.com/"><img src="https://static.slid.es/images/slides-github-banner-320x40.png?1" alt="Slides" width="160" height="20"></a>
</p>

reveal.js is an open source HTML presentation framework. It enables anyone with a web browser to create beautiful presentations for free. Check out the live demo at [revealjs.com](https://revealjs.com/).

The framework comes with a powerful feature set including [nested slides](https://revealjs.com/vertical-slides/), [Markdown support](https://revealjs.com/markdown/), [Auto-Animate](https://revealjs.com/auto-animate/), [PDF export](https://revealjs.com/pdf-export/), [speaker notes](https://revealjs.com/speaker-view/), [LaTeX typesetting](https://revealjs.com/math/), [syntax highlighted code](https://revealjs.com/code/) and an [extensive API](https://revealjs.com/api/).

# [Get Started](https://revealjs.com/installation)

# BBC Fork

This is the BBC fork of reveal.js and includes BBC styling including the Reith fonts
and BBC blocks. To be used for BBC presentations only.

## Using BBC styling

Include this:
```
		<link rel="stylesheet" href="dist/theme/bbc.css">
```

## Using accessibility helper

Include CSS file in the `<head>` of `index.html`:

```html
<link rel="stylesheet" href="plugin/accessibility/helper.css">
```

1. Include JavaScript file as dependency in `index.html`:

```javascript
<script>
// More info https://github.com/hakimel/reveal.js#configuration
Reveal.initialize({
  dependencies: [
                  { src: 'plugin/accessibility/helper.js', async: true, condition: function() { 
                    return !!document.body.classList; 
                  } 
              }]
});
</script>
```

### Features

#### Hidden offscreen slides

This plugin adds CSS to "really hide" offscreen slides using `display: none;` on an element wrapping each slide. This technique was used to avoid issues with transitions and `display: none`. For this to work, the styles must be loaded in HTML as a `<link>` tag (as opposed to injecting dynamically with JavaScript).

#### Dynamically labeled slide sections

HTML `<section>` elements commonly used for slides will act as landmarks in screen readers. To make them easier to identify, this plugin dynamically adds an `aria-label` property with a value of "Slide 1", as an example. For nested slides, it will add "Slide 1, child 1" with numbers relative to that slide.

Purpose: uniquely labeled sections are more useful in assistive technology than `<section>` soup.

Before (your code):
```html
<section>Reveal.js</section>
<section>
	<section>It might be dated</section>
	<section>But it's still useful</section>
</section>
```

After (dynamically rendered code):
```html
<section aria-label="Slide 1">Reveal.js</section>
<section aria-label="Slide 2">
	<section aria-label="Slide 2, child 1">It might be dated</section>
	<section aria-label="Slide 2, child 2">But it's still useful</section>
</section>
```

# Reveal.js

Want to create reveal.js presentation in a graphical editor? Try <https://slides.com>. It's made by the same people behind reveal.js.

## Upgrading from previous versions
Note that there are breaking changes relative to previous versions. See the [Upgrade instructions](https://revealjs.com/upgrading/) for more details.

### Getting started
- 🚀 [Install reveal.js](https://revealjs.com/installation)
- 👀 [View the demo presentation](https://revealjs.com/demo)
- 📖 [Read the documentation](https://revealjs.com/markup/)
- 🖌 [Try the visual editor for reveal.js at Slides.com](https://slides.com/)
- 🎬 [Watch the reveal.js video course (paid)](https://revealjs.com/course)

--- 
<div align="center">
  MIT licensed | Copyright © 2011-2024 Hakim El Hattab, https://hakim.se
  BBC specific material is Copyright (C) 2020 BBC
</div>

