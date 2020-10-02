====================================
Python scrabing news article with Newspaper3k
====================================
SimplyNews design to give best article details with Newspaper3k repo

* `Source code @ GitHub <https://github.com/s4birli/spinrewriter>`_
* `Releases @ PyPI <https://pypi.org/project/SpinRewritterPyt#downloads>`_


Install
=======

Install into your Python path using `pip` or `easy_install`::

    $ pip install SimplyNews
    $ easy_install SimplyNews


Usage
=====

After installing it, this is how you use it::

    Initialize SimplyNews.
    >>> url = "https://www.bbc.co.uk/news/uk-scotland-54379026"
    >>> from SimplyNews import SimplyNews
    >>> simplynews = SimplyNews(url, 'en')

    Request processed raw_news
    >>> simplynews.raw_news()
    text = simplynews.text

    Request processed cleaned_news
    >>> simplynews.cleaned_news()
    text = simplynews.text 
    #removed all images, links, emails from text
    # also replaced all h2, h3, h4 tags with [h2], [h3], [h4]

    Request processed prettier_news
    >>> simplynews.prettier_news()
    text = simplynews.text 
    #removed all images, links, emails from text
    # also aded all h2, h3, h4 tags to text

    Accessible parameters:
    text
    original_text
    original_html
    keywords
    desc
    title
    top_image_url
    images
    published_date = None
    authors