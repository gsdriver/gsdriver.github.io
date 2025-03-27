# Top 5 Benefits of the Jargon SDK for Voice Content Management

###### *January 28, 2019*

<p align="center">
  <img height="400" alt="Photo by BENCE BOROS on Unsplash" src="./images/jargon-benefits-hero.png">
</p>

I’ve published over a dozen Alexa skills over the last few years. Part of building a successful portfolio of voice applications is making sure I focus on the conversational aspect of my skills. I’ve also brought several of my skills into international markets such as Germany and Mexico to help ride the wave of Alexa’s expansion into these markets. To help me meet these goals, I’ve partnered with Jargon as an early customer. They are a startup that provides an SDK to help manage voice content across Alexa Skills, Google Assistant Actions, and the cross-platform Jovo framework. While their initial product offering is localization, adopting the [Jargon SDK](https://www.npmjs.com/package/@jargon/alexa-skill-sdk) has great benefits to help you manage your content even if you don’t plan to localize.

At its core, you work with the Jargon SDK by extracting the voice content from your code and putting it into a separate JSON file. Once you’ve done this, the SDK provides several benefits to iterate and perfect your content independently from your code. To illustrate these benefits, I’ll use the example of a pizza restaurant skill that lets you order a pizza, salad, or drink.

**1. Variation of Responses**

Adding some variety to the output from your Alexa skill is a great best practice to keep your skill from sounding stale — especially for responses that are part of your “common path.” The Jargon SDK allows you to do this by turning a single string in your JSON file into an object with several variations. The SDK will then randomly select one of the variations to put into your code! Rather than always hearing “What type of pizza would you like to order?” you can vary the response to alternately say “Which of our pizzas are you craving today?”or “Tell me what type of pizza you’d like today.”

**2. Pluralization**

A minor frustration that can throw off an otherwise engaging experience is not providing a singular form in a response (for example, saying “you ordered one pizzas”). Rather than adding checks for this in your code, the Jargon SDK allows you to modify your content to handle plural cases. In addition to the simple case of differentiating “pizza” from “pizzas,” you can also provide an entirely different experience for certain values. For example, your skill can respond “you ordered one pizza,” “you ordered two pizzas,” or “no pizza today? Maybe next time” just by tweaking values in your content file.

**3. Tailored responses to specific paths**

A side benefit of going through the process of extracting your content into a separate file is that it forces you to structure your code to pull in a single response to a specific path. You can take advantage of this to provide a streamlined response to a customer. For example, you may be repeating an order to a customer by concatenating the type of pizza ordered (if any), salad (if any), drink (if any) and total due in a response like “You ordered a pepperoni pizza. You ordered a large salad. You ordered a two liter bottle of soda. The total is $12.” Instead, you can acknowledge their complete order by saying “Thanks for ordering a full meal with a pepperoni pizza, large salad, and a two liter bottle of soda to wash it down for only $12.”

**4. Built-in Responses to Common Requests**

While platforms like Alexa have built-in intents to cover a variety of user input (such as an intent which covers multiple variations of “Yes”), they don’t provide built-in variants to respond to the user in common use cases. Jargon recently released functionality to fill this gap for two specific use cases. Analyzing many of the leading and most engaging Alexa skills, Jargon now provides variants to the most popular responses for:

* Cases when you receive user input that you can’t process
* A generic, non-contextual reprompt

With the SDK, you can use a special ID for these scenarios and not have to manage this content yourself.

**5. Localization**

If you’re going to engage with localization services of any kind, whether through Jargon or another provider, they’ll want to see your resources separated from your code. There is a growing international market for voice and by using the Jargon SDK which forces this content separation, you’ll be positioned to tap into this customer base.

Hopefully you found these benefits useful and decide to try out the Jargon SDK for your own voice application development! Let me know about your experiences in the comments!

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
