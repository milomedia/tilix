---
layout: post
title: "Making a website that’s more than a glorified business card"
date: 2016-12-23
---
During the Xmas holidays in 2016 I was inspired by "Inbound & Content Marketing Made Easy" by [Marcus Sheridan][1]. I found common sense in what the [The Sales Lion's][2] had to say and was pleased that it fitted with my many years experience of developing websites. 

To be blunt, www.tilix.uk was just a glorified business card. Granted, this was deliberate decision and I knew that one day it it would have to be transformed. Putting Marcus's wisdom into practice the following plan emerged:

  1. Optimise the homepage to work for both first time and return visitors
  2. Produce a constant stream of fresh content
  3. Use web forms to convert visitors to leads
  4. Collect and reflect regularly with beefy analytics that track leads

I saw the project as more than website development. Rather,  given the growing importance of marketing for Tilix, it was framed as a strategic imperative.

## The Guiding Principles
Unlike the previous build of www.tilix.uk, the aim this time around was more than producing a simple web page. Rather it was to marshal the people, tools and processes that can deliver a constant stream of content for discerning energy industry professionals. Specifically:

1. Help a first time visitor, within 10 seconds, to get a feel for the services offered by Tilix.
2. Convert visitors to leads with content that helps them overcome their energy challenges.

Fast feedback was vitally important to the project. In agile terms, the team were encouraged to release early and often. In Theory U terms we prototyped!

## The People and their Buddies
Tilix is a small team with a variety of skill sets. In order to get everyone contribution we had to lower technical barriers where possible.

In practice nobody can be an expert at everything, so we ran with buddy relationships. This was somewhat similar to pair-programming with one person being the driver and the other being the navigator.

We had buddy pairings in the following areas: 

- **Architecture:** The objective for this pair was to ensure that the *enterprise* requirements of broad-based collaboration from the whole team was met.
- **Coding:** This pair had to ensure that technical demands such as W3C standards, performance and maintainability were met.
- **Copy Writing:** The challenge here was to produce an order of magnitude more words than we had in the old website and to keep inline a content style guide (which we did not have before).
- **Graphic Design:** Relative to the old way of working, there was not much change here. The look and feel of the home page stayed the same and the design input on the new internal pages was minimal. The stretch objective was to create a written style guide.
- **Test & Review:** In order to identify when the site was ready to launch, this pair worked through a continuous cycle of inspection based testing and reviews from customers.

## The Content
The old website comprised one page with about five hundred words. The revised website had a dozen pages and just under ten thousand words at launch. Going forwards we expect to add 5,000 words per month. The content types include:

- Homepage
- Blog
- Brochure Pages
- Forms

### Homepage
It is no surprise that there is an army of consultants and authors with tips, tricks and advice on homepage design. The help and advice on how to get the most out of your prime real estate covers a wide range of topics including copy writing, graphic design, typography, psychology, analytics, usability, accessibility etc. 

We avoided the temptation to over analyse and we decided to stick with the simple wisdom of the Sales Lion:

>Within 10 seconds of being on www.tilix.uk, can a first time visitor

>1. Understand that we are able to solve their problem?
>2. Know where to go to get the answers?

On reflection, the old home page did not come close to passing this test. For example, many first time visitors assumed Tilix was an energy supply company. 

Despite the overall weakness, we felt improved copy writing was the answer. For example, the new headline we chose was:

![Headline screen grab]():

It was: 

>INNOVATION IN ENERGY SUPPLY & DEMAND - Making Energy Cheap, Clean and Cheerful

We decided that typography and styling would stay as is. However, we did introduce a new set of icons.

![Old site screen grab]()

![New Site screen grab]()

### Blog
A key objective is to produce a constant stream of fresh content and we are doing this through a *blog*. Video and other informational works will come later.

We decided that at launch we would have five or six posts. We had a healthy debate about style and settled on the following guidelines:

-  The corporate objective of the blog is to create B2B leads for Tilix. It is a core pillar of an _authority marketing_ based strategy for business development.
-  The core area of expertise is innovation & technology in energy.
-  Readers will want to learn from our work at the cutting edge of the transformation of smart energy. They want ideas, opinions, analysis and recipes that are thought leading.
-  Readers will only trust the Tilix Blog if the quality is high. Our expertise in the energy domain and in technology solutions must shine through. Content must be valuable to the audience. That means is timely, technically accurate and addresses real world challenges.
-  Posts will have cutting edge content but the tone of voice will be informative. Language will be as simple as possible but we must avoid being simplistic.
-  Readers will not want technobabble in business posts and hot-air in tech posts. There should be no criticism of competitors. Personal asides should only be used to colour in business and technical concepts.
-  Posts should be at least 500 words and less than 1600 words.

The most contentious point in this list was the guideline on the length of the post. We settled on our numbers based on the fact that 75% of blogs on Medium.com take less than 3 minutes to read and 94% take less than 6 minutes to read. It is also generally accepted that long posts should be avoided. They take more time to produce and are more difficult for readers to engage in. We plan to regularly review this guideline.

Previously we had decided to only publish posts on LinkedIn. Now, we have decided emphatically that the primary destination for our writing is www.tilix.uk and we will repost on LinkedIn.

We will also keep an open mind about reposting on other platforms. We currently favour Medium and will more than likely repost there as well as on LinkedIn.

### Forms
Forms will take an increasingly important role in www.tilix.uk because they underpin:

- Comments
- Surveys & Questionnaires
- Calls to Action
- List Subscription
- Customer Enquiries

However, in the first release the only changes we made were to:

1. Made the contact form a standalone page (so we can get far more granular visitor analytics).
2. Included Disqus comments in the blog.
3. Introduced a very low number of lead capture pop-up forms. 

## The Technology
These days it is not just IT people that are interested in nuts and bolts details. In the digital world HTML, CSS, Wordpress etc have become part of the staple diet for marketeers.

### Beefy Analytics
An analytic approach to managing websites will help formulate online strategy and validate performance. It is a no-brainer that any professional website should:

- Collect usage data
- Calculate metrics from usage data
- Track metrics over time

The legacy website used both page tagging (Google Analytics) and   web server log file analysis (with Qloudstat). The new website now also uses customer lifecycle analytics (with Hubspot).

Hubspot provides visitor-specific measurements that are enabling Tilix to use a variety of inbound tactics. In particular, website visits can be readily connected with to CRM contacts and clicks in outbound emails. This colours in the marketing and sales funnels as well as illuminating visitor behaviour and areas where website optimisation is needed.

### Static is the New Dynamic
The legacy website was hosted on Amazon S3 and the code was handcrafted with programming tools. This was good for a single page, glorified business card for a small IT firm with software engineers on the payroll. 

However, for the amount of content in the new site and a growing team of contributors this simple approach would not cut it. The alternatives considered were:

- Go dynamic with a self-hosted CMS (e.g. Drupal, WordPress, Joomla)
- Use a SaaS service (e.g. Wordpress.com, Squarespace, Jimdo, Wix.com, Virb
- Use Desktop applications (e.g. Dreamweaver, ToWeb, EZGenerator) that have WYSIWYG editors for building websites.
- Use a [Static Site Generator](https://www.staticgen.com)

We decided on the latter and stay in the good company of many others who realise that ["Static Website Generators Are The Next Big Thing"](https://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/). Advantages of static sites include:

- **Performance:** There are no server-side scripts and no database to connect to. Pages are served very quickly and the website has a very high throughput.
- **Hosting:** It is cheap and easy because there is no complicated setup or maintenance. It's also very sweet that there are excellent free options (e.g. GitHub Pages, Amazon S3, Surge.sh).
- **Security** Hackers love server-side scripts and databases. Flawed coding and failure to sanitise input to and output from a CMS are root causes of SQL injections and cross-site scripting attacks. These threat vectors just don't exist for static sites.
- **Content versioning** It is very easy to work with a version control system and to enable distributed authoring with GitHub or BitBucket.

All of these are compelling reasons but the most important factor for Tilix is **Markdown**.

Markdown is an easy-to-read, easy-to-write plain text format. Documents written in Markdown are easily converted to snippets of web content or entire web pages.

Writing web content using Markdown is a breeze. You just need a simple text editor. That could be at your desk, in your tablet or on your phone.

Our basic distributed content writing workflow is:

1. Write early drafts using an editor of your choice. (Our favourite is [IA Writer](https://ia.net/writer/)).
2. Save draft markdown files in a Dropbox share for editorial review.
3. Commit markdown files for pre-production review. The content is now public on www.tilix.uk but it does not show in RSS or the blog index page.
4. Publish the post. This makes it visible on the RSS feed and the index page.
5. Repost on "markdownified" platforms e.g. Medium.com
6. Repost onto "non-markdownified" platforms 

Steps 3 and 4 leverage Jekyll and Github Pages. Jekyll is probably a very popular static site generator and GitHub Pages provides website hosting plus an excellent team environment including source code repository, issues log and a wiki.
	
## The Result
Given time our customer surveys and analytics will clearly spell out if this project has delivered on its mission. Based on a little bit of early feedback, we are confident that www.tilix.uk is on the right track.

///*****///
**QUOTES HERE FROM TEST & REVIEW**
///****///

[1]: https://www.linkedin.com/in/marcussheridan
[2]: https://www.thesaleslion.com
