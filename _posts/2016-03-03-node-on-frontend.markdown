---
layout: post
comments: True
title:  "Node.js for front-end development"
date:   2016-03-03
categories: [software engineering, node, front-end, npm]
---

About a week ago, a question came up among my friends - "when people refer to
node being on the frontend...i'm confused...to me: node === backend".
I guess most of the time, Node.js is associated with back-end development and
that is because Node.js was originally built to make developing of scalable
applications easily by allowing us to write JS code that runs in a server
environment. Because of that reason, it seems that whatever projects that include
Node.js are often considered as just Node.js projects and nothing more.
But Node.js has other handy usages and in this post, I am going to attempt to
explain how Node.js can be used for front-end projects.

**DEVELOPMENT AND PRODUCTION WORKFLOW**:

You can use npm for front-end development and npm is Node.js's package manager,
hence, using of Node.js on the front-end.
Let's say I want to create a simple project that contains JS, CSS, and HTML
files and use Node.js to set up and run development tools and tasks. I would
normally start by running npm init in my command to generate package.json. Then,
I would create index.html and make CSS and SASS folders.

Folder Layout: CSS/app.css, SASS/app.scss

Because I've created CSS and SASS folders, I want to be able to compile SASS
into CSS. To do this, I can go to the package.json file and then under "scripts",
I can declare a npm command - ex: 'compile-sass' that I can use later in my
terminal (see below for implementation).

{% highlight javascript %}
"scripts": {
	"compile-sass": "sass --watch sass/app.scss:css/app.css"
}
{% endhighlight %}

As you can see from the implementation above, I can then just open up terminal,
type in 'npm run compile-sass' and whatever code I wrote in SASS will be compiled
and put into app.css. And I can do the same process to run Uglify to minify my JS
code or to run Browserify to bundle all the modules I am using.

**Takeaways**:

Node.js can run on a server but you don't have to make your projects rely on
a Node.js prod-environment. As seen from the example above, you can use Node.js
to set up development and production workflow. So Cool!
