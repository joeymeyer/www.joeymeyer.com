---
layout: post
title:  "Tumblr to Day One"
date:   2013-10-13
categories: tumblr dayone
---

A few years ago I had to opportunity to travel through Europe on a backpacking trip with my wife. During the trip we kept a journal of our travels on a Tumblr blog.

In the past year I have discovered [Day One](http://dayoneapp.com), a great journaling app for Mac and iOS. I try to use it daily to keep track of events, big and small, in my life.

A few months ago I realized it would be great to include the posts from the Tumblr blog we kept while in Europe in my Day One journal. There isn't a built in way to do this, but thankfully the Day One team created a simple [command line tool](http://dayoneapp.com/tools/cli-man/) to interface with your journal. I took the logical next step and wrote a script to pull down Tumblr posts and add them to the journal. It's open source and [hosted on GitHub](https://github.com/joeymeyer/tumblr_to_dayone), so feel free to make contributions if it's missing a feature you want to see.

It should work with all Tumblr blogs, and it's easy to use. You just need Day One installed on your Mac along with the [Day One CLI](https://dayone.zendesk.com/hc/en-us/articles/200258954-Day-One-Tools). To get started just:

  `$ gem install tumblr_to_dayone`
  
Once installed you can start it. I'll show you how to add posts from the [official Tumblr blog (staff.tumblr.com)](http://staff.tumblr.com) in this example:

{% highlight bash %}
$ tumblr_to_dayone

What is the name of your tumblr blog? (<name>.tumblr.com)

staff     # staff.tumblr.com

What is the password of your tumblr blog? (leave blank if none)

          # left blank because it's a publis blog

Automatically add all blog posts? (y/n)

n         # if you choose 'y' it will automatically add all of your posts

What is the location of your Dayone.journal? (leave blank if it is in the default location)

          # left blank because I want to add the posts to the journal currently used by the Day One app
{% endhighlight %}

After this step it will ask you one by one if you would like to add each post as an entry to your journal.

{% highlight bash %}
- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 

Tumblr post created on 2013-10-10 04:33:28 +0800

title: <no title>

photo: true

body:

새소식!


Tumblr is live in Korean!


Now you can blog in thirteen languages — just switch your settings [here](https://www.tumblr.com/settings).


For updates about Tumblr in Korean [follow our newest Staff blog](http://hangulteam.tumblr.com/).


대박!


\#features

- - - - - - - - - - - - - - - - - - - - - - - - - - - - - - 

Would you like to add this post to Day One? (y: yes, s: yes and star it, n: no, exit: exit the prompt)

y

...

{% endhighlight %}

It will continue going through all of the posts until there are no more or you type `exit`. Then open up Day One and all of your new entries will be there.

<img src="/img/tumblr_to_dayone.png" style="max-width: 100%; width: auto; height: auto;" />

This worked great for me, I was able to import all my blog posts from my Europe trip to my journal. Hope you guys can find a use for it as well. If you have questions or have feedback [send me an email](mailto:contact@joeymeyer.com).

Enjoy!

