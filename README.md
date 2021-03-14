HugoTufte is a bare-bones theme for [Hugo](https://gohugo.io/) that implements the design specified in the [Tufte CSS](https://github.com/edwardtufte/tufte-css) project. If you're familiar with Hugo, a quick inspection of the theme will reveal that it doesn't generate the list pages that are typically used to navigate a site. This is on purpose. The Tufte CSS project provides a layout for articles only, so HugoTufte follows suit. Because of this, HugoTufte is best used as a starting point for your own theme. It provides templates and shortcodes to work with the `tufte.css`. As an example, [Motif](https://github.com/kevinkenan/motif) uses the HugoTufte shortcodes with a CSS based on `tufte.css`.

I've used the features of HugoTufte to re-implement the self-describing demonstration document included with the Tufte CSS. The original, written in HTML, can be found in the Tufte CSS project: [index.html](https://github.com/edwardtufte/tufte-css/blob/gh-pages/index.html). The HugoTufte implmentation is located in the `exampleSite/` at [`exampleSite/content/tufte.html`](https://github.com/kevinkenan/hugotufte/blob/main/exampleSite/content/tufte.html).

HugoTufte requires that the site config include the `unsafe: true` setting for the Goldmark renderer. This is mainly to support block quotations with attributions because the attributions use nested shortcodes that contain HTML. There are ways to avoid this and achieve the same layout, but they would require changes to `tufte.css` which is contrary to my goals with this particular project. 