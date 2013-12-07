flasky
======

Pelican theme I created for fjavieralba.com
Feel free to add and also tweak it and add more features to it


In order to correctly use this theme you will need this variables in your pelican conf.py::

    AUTHOR = u'Your Name'
    SITENAME = u"Your site name"
    SITEURL = 'blog'
    TIMEZONE = "Europe/Madrid"

    #Navigation sections and relative URL:
    SECTIONS = [('Blog', 'index.html'),
            ('Archive', 'archives.html'),
            ('Tags', 'tags.html'),
            ('Projects', 'pages/projects.html'),
            ('Talks', 'pages/talks.html'),
            ('About', 'pages/about-me.html')]

    DEFAULT_CATEGORY = 'Uncategorized'
    DATE_FORMAT = {
    'en': '%d %m %Y'
    }
    DEFAULT_DATE_FORMAT = '%d %m %Y'

    DISQUS_SITENAME = "your_disqus_user"
    TWITTER_USERNAME = 'your_twitter_user_without @'
    LINKEDIN_URL = 'http://es.linkedin.com/in/you/en'
    GITHUB_URL = 'http://github.com/you'
    FACEBOOK_URL = 'http://www.facebook.com/you'
    GOOGLEPLUS_URL = 'https://plus.google.com/your_profile_id/posts'
    PINTEREST_URL = 'http://pinterest.com/you'

    PDF_GENERATOR = False
    REVERSE_CATEGORY_ORDER = True
    LOCALE = ""
    DEFAULT_PAGINATION = 10

    FEED_RSS = 'feeds/all.rss.xml'
    CATEGORY_FEED_RSS = 'feeds/%s.rss.xml'

    OUTPUT_PATH = '/your/output/directory'

    GOOGLE_ANALYTICS_ACCOUNT = 'UA-00000000-1'

    PIWIK_URL = 'myurl.com/piwik'
    PIWIK_SSL_URL = 'myurl.com/piwik'
    PIWIK_SITE_ID = '1'

    MAIL_USERNAME = 'your_user'
    MAIL_HOST = 'gmail.com'

    # static paths will be copied under the same name
    STATIC_PATHS = ["images"]

    # A list of files to copy from the source to the destination
    #FILES_TO_COPY = (('extra/robots.txt', 'robots.txt'),)



For more information about the Pelican settings you can visit http://docs.getpelican.com/en/3.1.1/settings.html#themes
i found them useful during the whole design process of the blog

Pelican comes with its own default theme, so when you want  download this theme .

First, choose a location to hold your theme. For this example, we'll use the directory ~/themes, but yours could be different. Clone the pelican-themes repository to that location on your local machine:

git clone https://github.com/fjavieralba/flasky ~/themes
Now you should have your pelican-themes repository stored at ~/themes/.

To use one of the themes, edit your Pelican settings file to include this line:

THEME = "~/themes/flasky"
So, for instance, to use the mnmlst theme, you would edit your settings file to include:

THEME = "~/themes/mnmlst"
Save the changes to your settings file and then regenerate your site by using the Makefile you should already have set up using pelican-quickstart:

make html
Themes can also be specified directly via the -t ~/themes/flask parameter to the pelican command. If you want to edit your theme, make sure that any edits you make are made to the copy stored in ~/themes/flask. Any changes made to files stored in your site's output directory will be deleted the next time you generate your site.

