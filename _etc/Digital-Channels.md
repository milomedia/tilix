---
layout: post
date: 2017-09-08
Author: Dave Hodgson
Primary SEO:  
Secondary SEO:
title: "Digital Channels for Small Suppliers"    
---
In addition to brand guidelines, style guides etc, small suppliers are interested in the following:

- **Website** - storefront type site that tells the world what the supplier does an why they should join etc
- **Customer Acquisition Portal (CAP)** - the sign up funnel which is embedded in the site above but more of a complex journey to ensure sign up
- **Customer Self Service Portal (CSSP)** - ability for customer to log in and have a my account function, ideally this should extend to a consistent mobile app as well

It helps to approach these as three separate problems (and scopes).

# Website
The bread and butter of digital agencies, most utilities websites follow a similar information architecture due in part to presenting some of the same information, but the flow and design through the information is different. This is not an area we look to deliver in but we do run the projects with external vendors. Agencies do this very well and don't need much industry knowledge to do it as long as they have someone injected that does have knowledge. Carving it off from the sign up means you can use basically any agency as long as they understand that their job is to guide 95% of users to either the CAP or CSSP - the remaining 5% probably just want extra info and then to be sent to the call centre or CAP.

The expensive part is typically the user journey, persona development and look & feel/Ux. The first two generally give a pretty similar result from the 5 we have done but are needed to ground the project and get started - that's why we've put some dummy personas together as a start point to try and skip some of the "visioning" type sessions. In terms of agency fees, for the static site alone you can probably expect 25-50k for a good product. I think the agency you have, or Jellyfish or Nodes would all do a good job on these, however they will try and cross sell into the CAP and CSSP which will result in the more eye watering quotes and probably a fairly painful delivery on those components.

# CAP - Acquisition Funnel
The single most important section for market entrants - its how you keep acquisition rates high and cost to acquire low. As you note, Octopus are great at this, other good ones are Ovo, Ecotricity, Engie, Bulb etc. The common thread they all have - get the customer detail with the least friction on the way, friction causes drop outs. However, they also give those users that want to for example refine with their actual numbers, compare tariffs etc, the ability to do that, not allowing that causes those that need more info when signing up to drop out, its a balance. There is a lot of merit in paying a Ux consultant to be involved in this process to get the flow just right, I know a contractor that worked for Jellyfish who has now gone independent and is the best Ux person I've worked with globally, I will check what he is up to now and see if he is interested with no commitment obviously.

The basic process is something along the lines of:

1. Get a postcode so you can get geographic pricing
2. Get a fuel choice so you know how to price (generally default to dual) _ Consider if you want to offer PrePay and Economy 7, if not then let them drop out early, don't collect the info then tell them they can't sign up_
3. Make some assumptions which most users won't change, but make it possible to change if they want to (number of rooms, kWH usage etc)
4. Provide a quote and option to sign up _ If you intend to list on switching sites, EHL power the majority of them, and run their own switching site, they cost about 20k per year for unlimited quotes/comparisons via their API, they do a good job but are painful relationship wise, I'd still use them_

_ I recommend you don't write a quote engine in house initially - high maintenance overhead, not least to keep data in them current and some level of upfront dev cost; similar or more than EHL, you can swap it out later as long as contract is easy to terminate

5. Collect information on the person, house etc

_ If collecting by Direct Debit then call a Know Your Customer type check (legally have to do this for BACS accreditation, again outsource this to BottomLine, WorldPay etc - probably whoever you use for DD processing or card payments_

_ If you are credit checking then call out to that seperately - Experian etc

6. Push all the information above into Junifer using either via their API call (preferable due to immediate response to user) or create a file like a switching site does and load into Junifer

_ If you will have CSSP at start, I cant recommend the API strongly enough, you should create a My Account immediately and get it activated, not doing so hurts customer adoption of the my account functionality

7. Provide feedback to the client on what happens next, get them to log into self service, or if they were rejected explain why etc._

The options here that I can think of are:

**Take Junifer or EHL's out of the box portal**

_ They are compliant, probably cost effective, will be branded with your guidelines within limits

_ BUT they won't be exactly as you like and will look basically like White Rose, Robin Hood or many others, poor outcome in my view

_ Likely cost: not sure, you will have the figure though, I'd guess in the 25-50k region_

**Use another company's out of the box portal**
Methodia for example do a nice job of this, again I have personal relationships with the CEO and founders so could introduce easily

_ They compete directly with Junifer & Utiligroup on Billing and Flows systems among other things, but the funnel can be deployed on its own and kicks out a file similar to a switching site file so Junifer will ingest it, we could then automate emails from Junifer for the sign up to the self service portal. Obviously if using their full suite it just does that bit for you.

_ They are compliant, the process is much nicer and more modern tech than the above, it will be low cost, branded easily and customisable to an extent (more than the above but I don't know how much), it could be up and going in a week or two

_ BUT it will still be customisable within limits, they also have a quick dev team and are flexible and hungry to get into the UK market; Bulgarian firm that have live customers in UK, Spain, Italy, Romania and Bulgaria, there will be future attempts to upsell the rest of the product set. The file being sent may lead to some delays in the sign up of the my account bit

_ Example at: [https://switch-corona.methodia.com/en/switch][1] (user is corona, password is boza1234)  for work they did for Corona it looks pretty slick_

   [1]: https://switch-corona.methodia.com/en/switch

_ Likely cost: not sure, maybe 15-20k upfront and a per sign up fee but would need to check_
