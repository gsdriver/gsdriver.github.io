# Why Your Startup should Invest in a Strong Technical Foundation

### Make your pivots easier by taking some design time upfront 

###### *February 15, 2022*

![The Child Care Concierge](./images/foundation-hero.png "The Child Care Concierge")

At [LegUp](https://www.legup.care), we recently launched The Child Care Concierge. It matches families to full-time and part-time child care by guiding them through the entire enrollment process. I helped co-found LegUp in 2019 with the vision to help families find and enroll in quality care for their children from pre-birth to pre-teen years. This release represents a significant milestone along that journey. But as with any startup, and especially those forming in the past few years, we pivoted a fair amount along the way. Our ability to shift our product through these pivots shows the importance of a well-architected design.

**Iterate Quickly but have a solid foundation**

![Moving fast](./images/foundation-fast.png "Moving fast")

As a startup, you have to be able to react based on learnings and changing market conditions. The last two years have seen a lot of changing market conditions, not only in child care, but everywhere! “Build fast” is a common war cry in the early days, and LegUp was no exception. Our first product release came three months after coding started. Despite this, I spent several weeks upfront thinking about the back-end database design. With so much emphasis on building, iterating, and planning to throw everything away as you learn, why would I do this?

Well, for one thing, I’m not a database expert. I have, since starting LegUp, learned a lot about Postgres database design. But when I started, I needed to make sure I understood basic database design and architecture. Taking time to read about design patterns and applying them to our own business practices helped me learn a lot. Sharing those ideas with my non-technical co-founder forced us to take those practices out of our heads and write them down. This in turn ensured a shared vision and removed ambiguities.

As we’ve grown, we’ve hired more specialists and today have an engineer with a stronger database background. He’s (appropriately) chastised my inefficient sprocs, poor indexes, and certain best practices. But he’s also said that the table design is pretty good. That was good to hear, because that has proven foundational to allow for quick pivots.

> It took three days — a weekend project — to build an MVP of a new product that helped us close our first round of funding

We help connect supply and demand. Over the past few years, that balance has shifted back and forth. As we’ve entered new markets, we’ve seen different customer needs because of this dynamic. If you’re creating a new UX experience or a whole new product offering, building on top of an existing foundation will save you weeks if not months. In late 2020, we launched a new product that showed potential investors a new direction. My co-founder credits it for helping close our first round of funding. It took three days to build this MVP — a weekend project on top of our existing infrastructure and data.

**Start with a reasoned technical foundation**

![A Strong Foundation](./images/foundation-foundation.png "A Strong Foundation")

I’ve advised several other startups, many of whom for lack of in-house expertise have outsourced their product development. That’s not a bad thing, provided the vendors know the right foundation. If you’re a non-technical founder, encourage them in the first few weeks to design and share that foundation with you. Walk through some business processes with them. Explain what you envision happening at each step. Do this before they write any code and make sure they understand your domain. It’s cheap at this point to make design modifications if necessary.

>The stronger your foundation, the easier it is to pivot and even completely change front-end product offerings

I’ve seen many startups instead provide some wire frames to an outsourced company. They may get something that looks like what they’ve asked for, but doesn’t quite fit their domain. Once they have a working codebase and paying customers, they feel the need to maintain that code base. It makes sense, you don’t want to leave your customers high and dry. But as I’ve learned with LegUp, the stronger your foundation, the easier it is to pivot and even completely change front-end product offerings. Unfortunately, many companies find themselves stuck needing to support something much more brittle.

Do yourself a favor, take the time to lay the right foundation. Whether you do this with in-house technical expertise, leveraging a technical advisor, or in-depth Q&A session with your vendors, you’ll be glad you did when the need to pivot comes.

***

#### Leave a comment

###### Comments are powered by Utterances. A free GitHub account is required. Please be respectful. No swearing or inflammatory language. No spam.
###### **I reserve the right to delete any inappropriate comments.**

<script src="https://utteranc.es/client.js"
        repo="gsdriver/gsdriver.github.io"
        issue-term="pathname"
        theme="github-light"
        crossorigin="anonymous"
        async>
</script>
