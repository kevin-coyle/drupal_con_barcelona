# Fundamentals of front end ops

- Intended for front end ops, not just Drupal.

[Preston So Website]http://preston.so

## Why Front End ops

Automation = consistency.
- Quality Testing.
- Better release management.

Abstractions and frameworks change the way that we work. These benefit from front end ops automation.

Application logic moved over from server to client side.

emph on process.

<blockquote>
Too much work on front end ops for FEDS to do everything on their own.
</blockquote>

### Today

Scaffolding is more complicated. Libraries and frameworks need to stay up to date.
Test suites and TDD. Integrated into CI tools like Jenkins.

### Workflow
Tools:
- Yeoman
- Bower
- Gulp/Grunt

How does this help us?

"Flexibility to customise your setup as much as you desire"

Limit the time spent writing boilerplate (Yeoman)

#### Yeoman
- Explicitly recommends a workflow that involves Bower, Gulp/Grunt.
- Yeoman uses generators e.g. angular or bootstrap
- Can do portions of apps
- CLI

#### Bower

- Dependency resolution
- CLI.

#### Gulp/Grunt
- Task Automaters
- Configuration that allows you to determine what they do.

## Installation

````
node -v
````

````
npm install -g yo bower gulp Grunt
````
###Bower

An already regd package

````
bower install jquery
````

From github
````
bower install drupal/drupal
````

Search

````
bower search
````

#### Yeoman

- See slides.

### Gulp and Grunt

````
npm install grunt-contrib-uglify --save-dev
````
Gulp is task execution. Grunt is desired state.


#### Useful plugins
- Grunt UnCSS
- Grunt uglify

With gulp you configure and reg. tasks in the same process.

## Regressions and rendering

- Visual Regressions
- Testing rendering engines
- Testing devices.

Comparisons between where on the page where the diffs lie. What pixels have changed.

CSS is prone to errors.

### Wraith

Snaps screenshots of pages.

### Huxley

Watches you browse and takes screenshots and tells you when they change.

## Ghost lab

Basically browsersync but costs more.
