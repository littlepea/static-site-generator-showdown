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

Let's create a default website following the [official documentation](https://github.com/eudicots/Cactus):

```commandline
pip install cactus
cactus create cactus_blog
cd cactus_blog
cactus serve
```

Open the site in a browser and see the default page:

![](https://www.evernote.com/l/AHRHrZvl5ANHZJyselR2vJ1iYyDTfRnuwH8B/image.png)

## Theming

...

## Extensibility

...

## Conclusion

...