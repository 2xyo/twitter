Python Twitter Tools
====================

|Build Status| |Coverage Status|

The Minimalist Twitter API for Python is a Python API for Twitter,
everyone’s favorite Web 2.0 Facebook-style status updater for people on
the go.

Also included is a twitter command-line tool for getting your friends’
tweets and setting your own tweet from the safety and security of your
favorite shell and an IRC bot that can announce Twitter updates to an
IRC channel.

For more information, after installing the ``twitter`` package:

-  import the ``twitter`` package and run help() on it
-  run ``twitter -h`` for command-line tool help

twitter - The Command-Line Tool
-------------------------------

The command-line tool lets you do some awesome things:

-  view your tweets, recent replies, and tweets in lists
-  view the public timeline
-  follow and unfollow (leave) friends
-  various output formats for tweet information

The bottom line: type ``twitter``, receive tweets.

twitterbot - The IRC Bot
------------------------

The IRC bot is associated with a twitter account (either your own
account or an account you create for the bot). The bot announces all
tweets from friends it is following. It can be made to follow or leave
friends through IRC /msg commands.

twitter-log
-----------

``twitter-log`` is a simple command-line tool that dumps all public
tweets from a given user in a simple text format. It is useful to get a
complete offsite backup of all your tweets. Run ``twitter-log`` and read
the instructions.

twitter-archiver and twitter-follow
-----------------------------------

twitter-archiver will log all the tweets posted by any user since they
started posting. twitter-follow will print a list of all of all the
followers of a user (or all the users that user follows).

Programming with the Twitter api classes
========================================

The Twitter and TwitterStream classes are the key to building your own
Twitter-enabled applications.

The Twitter class
-----------------

The minimalist yet fully featured Twitter API class.

Get RESTful data by accessing members of this class. The result is
decoded python objects (lists and dicts).

The Twitter API is documented at:

**http://dev.twitter.com/doc**

Examples: \`\`\`python from twitter import \*

t = Twitter( auth=OAuth(token, token\_key, con\_secret,
con\_secret\_key)))

Get your “home” timeline
========================

t.statuses.home\_timeline()

Get a particular friend’s timeline
==================================

t.statuses.user\_timeline(screen\_name=“billybob”)

to pass in GET/POST parameters, such as ``count``
=================================================

t.statuses.home\_timeline(count=5)

to pass in the GET/POST parameter ``id`` you need to use ``_id``
================================================================

t.statuses.oembed(\_id=1234567890)

Update your status
==================

t.statuses.update( status=“Using @sixohsix’s sweet

.. |Build Status| image:: https://travis-ci.org/sixohsix/twitter.svg
   :target: https://travis-ci.org/sixohsix/twitter
   .. |Coverage Status| image:: https://coveralls.io/repos/sixohsix/twitter/badge.png?branch=master
      :target: https://coveralls.io/r/sixohsix/twitter?branch=master)
