---
layout: post
title: "Distributed Consensus"
---

I wanted a refresher on Google Spanner core concepts, so I generated myself a 15 minute podcast from [the Spanner whitepaper](https://static.googleusercontent.com/media/research.google.com/en//archive/spanner-osdi2012.pdf).
Let me see if I understand the concept.
In order to do that I will try to explain why Spanner is a big deal to a reader that may not be very well versed in databases.

Simply put a **database** is a software system where we can store data, and then ask to retrieve it.
If you are buying things online, and see a list of products, underneath is a database of products, and they are listed there according to some rules.
Similarly if you are getting products related to the text you type in a search box, underneath a *query* finding products related to the search has executed.
If you see the same product in your shopping cart on mobile device that you added on a laptop that is result of a write (*product is in the user's cart*) and a read (*show products in user's cart*).

OK, so we understand how databases work, roughly.
Imagine though that you add an item to your shopping cart.
Then if you read the items in that same shopping cart, you would expect to see the item you just added.
This property of a database is called **consistency**.
So fundamental, we would not even think of it, right?
As weird as it may sound, the following are true:

* *Many* databases *do not* provide strong consistency guarantees.
* Oftentimes this fundamental property may need to be traded for other desirable properties (more on that later).
* Providing good user experience, and an appearance of a consistent system on top of a database without this property requires tremendous engineering effort.

(to be continued)
