---
layout: post
title: Wikimedia Week 5
---

Going into week 5, things have been slow. The two weeks in between this post and the last coincided with the winter break for staff at the Foundation. Consequently, I've been less active, though I have been scrupulous about keeping to my two articles published per week.

The official theme for this week's blog is, "Explain your project to a newcomer to your open source community." To be honest, it's somewhat similar to my project as a whole.

My job at the Foundation is to explain how to use MediaWiki to a broad audience of users. In practice, this means updating all our action API docs to be more consistent, informative, and readable, as well as creating a web app to serve as both an example and a tutorial.

[MediaWiki is the software many wikis run on](https://www.mediawiki.org/wiki/Manual:What_is_MediaWiki%3F). This includes our friend, Wikipedia. In fact, the software was originally created to run the English Wikipedia.

The action API is a system for interacting with MediaWiki. It uses web requests to communicate what to do. The beginning of the request is the address of the web server that's hosting the wiki. The rest of the request is a set of parameters, indicating the action you want to take.

You compose your query, the server reads the parameters, and then it performs the request (or doesn't).

Then it sends back a response. 

All of the documentation for the action API is hosted on [MediaWiki.org](https://www.mediawiki.org/wiki/MediaWiki). The documentation includes individual pages dedicated to every single parameter. Within these parameter pages, there are currently inconsistencies in formatting, in how much and what kind of information is included, and in what languages are used to present sample code for requests. This is especially a problem for very popular pages, which have high visibility and high potential to confuse readers. 

I am going through the top 50 most viewed pages on MediaWiki.org, formatting the parameter pages to fit a template, and adding sample code in Python, to demonstrate how to use each parameter in a request. All of my sample code is also included in [a Github repo](https://github.com/srish/MediaWiki-Action-API-Code-Samples), hosted by my mentor, [Srishti Sethi](https://www.mediawiki.org/wiki/User:SSethi_(WMF)).

The process starts by reading over a page, then creating a draft for it in my sandbox, which is MediaWiki's name for areas of the wiki where users can test out ideas in a semi-private environment. Sandboxes are only private by obscurity -- they're subpages off of your own user page, and anyone can view or edit them if they know the address.

Once I start a draft, I copy and paste the template for the action API. "Template" is, perhaps, a misnomer here, because MediaWiki also uses the term "template" for special syntax which automatically generates text and markup. The action API template I use is more like a skeleton of markup, which requires me to manually add text from the target page within each section. 

My work includes editing pages to be easier to read. I would go as far as to say that most of my time is spent re-wording what is already there, and tightening up passages where I see fit. The docs often suffer from over-explaining the simple, and under-explaining the complex. This is very much a general problem of technical writing, not just the docs on MediaWiki.

I also perform research to ensure the information on the page is accurate. Sometimes this means falling down rabbit holes, as I try to track down the changes between API versions, or figure out how to explain technical terminology to newbies. 

The sample code also follows its own template, and uses the popular [Python requests library](http://docs.python-requests.org/en/master/). It is usually not so hard to write, with the main difficulty being in finding good Wikipedia pages to demo each query. For example, for the page [API:Allimages](https://www.mediawiki.org/wiki/API:Allimages), I spent a lot of time hunting for images whose file names followed a sequence, so as to make it clear how the response was ordered.

Once I have fit the page to the template, written the sample code, and edited it to a satisfactory level, I send my mentor a link to the draft. She reads it over, gives me advice, and I make any changes she asks of me. After a second overview, the page goes live: I copy and paste the source for the draft into the page on the main site.

I copy and paste all at once because this makes it much easier for other editors, especially the translators. MediaWiki has a translation system which uses tags associated with each paragraph. This divides the page into modular sections. 

Because the tags are generated in a fixed order, they can make re-arranging the page for clarity and consistency much harder. It can also be very confusing for translators when an editor comes in and makes many small changes by re-arranging, adding, and removing paragraphs in quick succession. 

For these reasons, I have been trying to avoid pages that already have been translation tagged. The translation admin, [Shirayuki](https://www.mediawiki.org/wiki/User:Shirayuki), tags my pages for translation after they are published.

I have 10 pages published on the main site, so far. Ideas for the tutorial app are still in the works, but the aim is to use several APIs to demonstrate log in, editing, retreiving information, and how to use the response to create something useful. 

You can track my progress on [my user page](https://www.mediawiki.org/wiki/User:Martyav). I try to be very meticulous about updating.

Well, that's it for now. By next post, I'll be half-way through my internship and almost ready to start serious work on the app.
