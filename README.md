pelican-theme-bootstrap3
========================

Bootstrap 3 based theme for Pelican. Used on my [blog](https://www.zoe.vc) - feel free to copy and adjust.
Texts are English.

Usage
-----

Download the [latest release](https://github.com/dArignac/pelican-theme-bootstrap3/releases/latest), extract and put the *bootstrap3* folder somewhere and point the THEME setting in your *pelicanconf.py* to this place. For example:

#
    THEME = '/home/me/pelican/bootstrap3/'

Also configure the Jinja2 extension "with":

#
    JINJA_EXTENSIONS = ['jinja2.ext.with_']


Code highlighting
-----------------

Pelican comes with [pygments](http://docs.getpelican.com/en/3.3.0/getting_started.html#syntax-highlighting) for syntax highlighting.
I do not want to always include the pygments css files, so it is only included if a post has the tag **code** (works on all pages).


Plugin support
--------------

Theme supports the following plugins:

* [Related posts](https://github.com/getpelican/pelican-plugins/tree/master/related_posts), displayed only on detail pages


Configuration
-------------

There are some minor configurations available (set within *pelicanconf.py*):

* COPYRIGHT: will display the set text on the page bottom, useful for a copyright info
* DISQUS_ID: if set to a value, will include [Disqus](http://disqus.com/) comment code
* EXCLUDE_TAGS_FROM_TAGCLOUD: list of tag names that shall not be included in the tag cloud. E.g. you might find it useful to exclude the "code" tag (see [Code highlighting](#code-highlighting)).

Release log
-----------

* 1.0.1
    * fixed wrong link to pygments stylesheet
* 1.0.0
    * fixed wrong package naming, now "extended_sitemap" instead "extended-sitemap"
    * added unit tests
    * raise ConfigurationError if TIMEZONE setting is not set
    * tags are now sorted by name
* 0.2.0
    * added categories to navigation
    * added [MENUITEMS](http://docs.getpelican.com/en/3.3.0/settings.html#themes) to navigation
* 0.1.0
    * initial release
