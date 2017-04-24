# Python Static Site Generators Showdown: Cactus, Pelican, Nikola, Lektor

Choosing a static site generator is easy in a way that any of them "gets the job done", 
at the same time, it's tricky because there are too many choices.
  
You can simply choose based on what matters to you the most:

* Pelican - if you want the most feature-full and actively supported
* Cactus - if you want an OSX GUI
* Lektor - if you want a CMS with an admin UI
 
But for me what really matters is the usability, so the only way to find out which one is the best is to try them all!

## Disclaimer

In this showdown we're going to compare the following 4 tools:

* [Cactus](https://github.com/eudicots/Cactus)
* [Pelican](https://github.com/getpelican/pelican)
* [Nikola](https://github.com/getnikola/nikola)
* [Lektor](https://github.com/lektor/lektor)

And compare them based on the following criteria:

* Ease of use / setup
* Theming
  * by integrating a [PureCSS](https://purecss.io/) based [blog example](https://purecss.io/layouts/blog/)
* Extensibility
  * by creating a plugin to show LinkedIn profile info
* Deployment (optional)
  
We only include Python tools because I want to be able to extend them (via plugins) and Python is my language of choice.

We purposely don't include [other tools](https://www.staticgen.com/) like [Hyde](http://hyde.github.io/), 
as it hasn't been updated in over a year, and [MkDocs](http://www.mkdocs.org/) or [Sphinx](http://www.sphinx-doc.org/), 
as I want to focus on blog/website use cases, not project documantation.

So, with that out of the way, let's begin!

## Ease of use / Setup

### Cactus setup

We could create a default website following the [official documentation](https://github.com/eudicots/Cactus):

```commandline
pip install cactus
cactus create cactus_blog
cd cactus_blog
cactus serve
```

But I've decided to use their [GUI for Mac](http://www.cactusformac.com/) application to create a Blog:

![](https://www.evernote.com/l/AHSfGR7DlSRL-43C2-jxsRIyNw1_hud6cB0B/image.png)

### Pelican setup

Let's do the same for Pelican following their [Quickstart guide](http://docs.getpelican.com/en/stable/quickstart.html):

```commandline
pip install pelican markdown
mkdir -p pelican_blog
cd pelican_blog
pelican-quickstart
```

It asked us a bunch of questions about new project and created some scripts 
as well as `content` directory where we can add our first dummy blog post `keyboard-review.md`:

```markdown
Title: My First Review
Date: 2010-12-03 10:20
Category: Review

Following is a review of my favorite mechanical keyboard.
```

Then we run the pelican command to generate our site:

```commandline
pelican content
cd output/
python -m pelican.server
```

And here it is in action:

![](https://www.evernote.com/l/AHQL3puW6V5BNLpTAvh7ojbYGAq3Y-56qGgB/image.png)

### Nikola setup

For Nikola we're following their [Getting Started guide](https://getnikola.com/getting-started.html):

```commandline
pip install Nikola
nikola init --demo nikola_blog
cd nikola_blog/
nikola build
nikola new_post -e
```

It created an empty blog post in `posts/my-first-blog-post.rst`.

Then I needed to re-build the site and start the dev server:

```commandline
nikola build
nikola serve --browser
```

And here we go:

![](https://www.evernote.com/l/AHRBbajZgrxIHLOazVcfjJKIafbAl0gczegB/image.png)

### Lektor setup

For Lektor I've also followed the [Installation](https://www.getlektor.com/docs/installation/) and [Quickstart](https://www.getlektor.com/docs/quickstart/) guide.

It should have been as easy as `pip install Lektor` but I've decided to go through their OSX app installation process 
by downloading a DMG, installing `Lektor.app`, opening it and running `Install shell command` option.

Then we can switch to CLI and start the new project:

```commandline
lektor quickstart
cd lektor_blog/
lektor server
```

And this is it:

![](https://www.evernote.com/l/AHQQAqgYz_ZGK4bLvCOrOmwmrI89q4JfQMgB/image.png)

### And the winner is Cactus!

Lektor was almost as easy to setup. Both have a very simple setup process and the OSX apps are very convenient.

Pelican was ok, Nikola was slightly annoying...

## Theming

Theming is probably the most important aspect in this evaluation, 
I don't think many people are going to be happy with the default themes of any of these sites 
so being able to customize easily is very important.

First, I've downloaded the [static files](https://purecss.io/layouts/blog/download) 
for the [blog layout](https://purecss.io/layouts/blog/) I've chosen 
and then start applying it to each of the blogs.

### Customizing Cactus

I had to:

* replace `templates/base.html` and `pages/index.html` with the contents of `index.html` 
* define all the necessary blocks like `title`, `content`, etc...
* copy the styles from `blog.css` to `static/css/style.css`
* fix the links to static assets with `{% static %}` template tag
* customize `templates/post.html` to display each single post correctly

That's it!

![](https://www.evernote.com/l/AHTCFI4hw45IDIJugmmaBAxlXdyAaE7g2EwB/image.png)

### Customizing Pelican

...

### Customizing Nikola

...

### Customizing Lektor

...

## Extensibility

...

## Conclusion

...