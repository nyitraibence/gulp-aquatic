# 🌊 &nbsp;&nbsp;gulp-aquatic

Aquatic is a gulp based forntend workflow optimized for classic sitebuild and wordpress theme development.


## Installation

For installation, you need to have [node.js](https://nodejs.org/en/) on your computer (to be able to use **npm**).

1. **Clone** the **repository** into a local folder
2. **Navigate** into that folder in the **command line**
2. if you don't have the global gulp-cli, install it:&nbsp;&nbsp; `npm install --global gulp-cli`
3. **Install** the project dependencies:&nbsp;&nbsp; `npm i`


## Usage
Two main tasks, accessible via the gulp-cli:

### `gulp watch` - for development

* Concatenates Js and SCSS Source files
* Creates a sourcemap
* Compiles SCSS to CSS
* Watches the files and reloads the browser on source change

### `gulp` - for production (default task)

* Cleans asset folder from 'leftovers'
* Concatenates Js and SCSS source files
* Compiles SCSS to CSS
* Minifies Js and CSS outputs
* Optimizes images

Some of these sub-tasks can be run separately aswell, if needed. See `gulp --tasks` for options. Easily extensible with additional features in the pipeline. You can find more help with this in the Gulp Documentation: [https://gulpjs.com/docs/en/getting-started/quick-start/](https://gulpjs.com/docs/en/getting-started/quick-start/)

### Notes:
- gulp-terser is used instead of popular gulp-uglify: In the field of Js compression terser shows slightly better performance, and it is ES6 compatible - uglify is not.
- Media query grouping is omitted from the pipeline. According to my researches, grouped/ungrouped media querys barely show any difference in performance, even in larger projects. And the less step there is in the pipeline, the faster, cleaner it is. Therefore, it is omitted.
<!-- 
Choosing BrowserSync over Livereload: It is not constrained to a single device, it works across desktop and mobile devices at the same time. It will update code changes, synchronize scroll positions and form inputs automatically across all browsers and devices. Also it doesn't need a browser plugin.
More: [https://www.slant.co/versus/5065/5066/~livereload_vs_browsersync](https://www.slant.co/versus/5065/5066/~livereload_vs_browsersync)
-->

#### To be added:
- cache busting
- error screens

***

The project is optimal for classic site building, and Wordpress theme development. For more 'Js heavy' projects, consider using a webpack configuration, as it is more suited for that.