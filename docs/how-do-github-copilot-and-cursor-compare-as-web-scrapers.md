# How do GitHub Copilot and Cursor compare as web scrapers?

### Taking two popular code generation tools for a spin

###### *April 24, 2025*

<p align="center">
  <img height="400" alt="Photo by Tai Bui on Unsplash" src="./images/scraper-hero.jpg">
</p>

I wanted to take two of the more popular code generation tools for a test spin – GitHub Copilot and Cursor. I decided to put these tools to my own test by asking them to create a web scraper. I decided to ask these tools to summarize the list of articles on [my blog site](https://blog.garrettvargas.com). I asked them to look at the page and summarize the article titles, URLs, and date of publication in a CSV format. Web scraping is a well-known problem with several public code examples. The information on my site is not in a tabular format, so there is some thought needed to extract the results. Finally, since I have experience with scraping, I could judge the generated code quality.

I started both projects with the same prompt. “Create a new project to scrape this website – https://blog.garrettvargas.com. It should return a list of article titles, the URL of the article, and the date of publication. This data should be saved into a CSV file format.”

<p align="center">
  <img height="400" alt="Blog Website" src="./images/scraper-site.png">
</p>

So how did these tools do?

## Initial Code Generation
### Winner: GitHub Copilot

Both tools came up with a good skeleton for a scraper written in Typescript using Puppeteer. They were similar, leading me to believe they may have used the same public examples as a baseline. Compared to Cursor, GitHub Copilot set up the project in a more robust and readable manner. It included more comments to explain the steps during the scrape. It also factored the code into classes which I felt made it more maintainable. Cursor put most functionality into a single function and with fewer comments.

GitHub Copilot’s extra factoring may have led to a bit much complexity. On my first run of the code, it didn’t build due to some import errors. GitHub Copilot was able to identify and fix these issues, but it was disappointing that the initial code didn't run.

## Debugging
### Winner: Cursor

<p align="center">
  <img height="300" alt="Photo by ThisIsEngineering on Unsplash" src="./images/scraper-debugging.jpg">
</p>

There must be public examples of a scraper that collects information about articles. Both tools generated code assuming a similar structure that didn’t exist on my page. They assumed my page had HTML tags with the name “article” or used `h2` tags around my titles. The comments that I liked with GitHub Copilot worked against it, as they were too authoritative. I would have preferred it if they suggested that I should verify the specific structure.

Debugging with Cursor was a breeze. It started autosuggesting prompts to run and test the code which I accepted. When it realized the initial code didn’t work, it tried several approaches to fix the problem. It added waiting for the JavaScript on the page to load. It used a curl command to download and inspect the content of the HTML. Unfortunately, this last step took it further off track. Something in the header caused Cursor to conclude this was a “typical Jekyll-based blog.” It then proceeded to use another set of incorrect selectors in the code based on this.

> Debugging with Cursor was a breeze. It started autosuggesting prompts to run and test the code which I accepted. When it realized the initial code didn’t work, it tried several approaches to fix the problem.

GitHub Copilot, meanwhile, struggled with the debugging process. It didn’t suggest techniques on its own but rather told me that I should inspect the HTML structure of the page to let it know the appropriate selectors. When I asked it to download the page itself, it refused forcing me to include the source of the HTML page as a prompt. Even then, it didn’t completely work. It saw the date as a sibling of the article link when there’s a subtitle between the two. It got stuck in a loop as I told it that selecting the date wasn’t working and to revisit how it was finding the date on the page. I finally had to debug myself to give it a prompt that would break it out of this loop.

## Solving the Problem
### Winner: Cursor

Of course, the real test is how well these tools were able to solve the initial problem. How much intervention did I need to provide, and at what level of experience?

While I was able to get a working solution from both tools, Cursor won this round hands-down. When it got stuck trying different debugging techniques, I gave it a manual prompt. “Read the HTML of the page so you can use the correct selectors. It’s not necessary to wait for JavaScript to load.” With this prompt it updated the code to a working solution. Besides the initial prompt to set up the problem, this was the only manual prompt I had to give Cursor. The rest of it was me auto accepting the suggestions from the tool.

GitHub Copilot, on the other hand, needed a lot more handholding. After several rounds of asking it to debug the problems it had with the relationship between HTML elements on the page, I gave it an explicit prompt. “The problem is that the \<strong\> tag is two elements after the \<p\> tag with the link. Can we use that to get the date?” Only after this rather direct prompt was it able to generate a working solution.

With Cursor, I only needed to guide its debugging approach. I didn’t need to review the code, and didn’t need to have in-depth knowledge of the structure of the page or the nature of web scrapping tools. I only needed to ask it to look at the content on the HTML page and that it wasn’t necessary for JavaScript to load. A non-developer might not know to ask it this, but it an entry-level developer without web-scrapping knowledge could figure it out. With GitHub Copilot, by contrast, I had to read through and understand the code before being able to give it a direct prompt. It took closer to senior-level guidance to get a working solution.

## Overall Pick
### Winner: Cursor

Both tools are impressive and rapidly evolving. Either one makes the programming experience better than nothing at all. In the end I felt Cursor was the better experience. Programming with Cursor felt more like mentoring a junior developer. It was curious and able to explore on its own but ultimately needed a hint from me to get back on track. GitHub Copilot felt more like traditional debugging, with me needing to be on top of and explicitly asking for changes. Had I not been able to read through the code and understand its assumptions, I would have been unable to complete this task with GitHub Copilot.

> Programming with Cursor felt more like mentoring a junior developer. It was curious and able to explore on its own but ultimately needed a hint from me to get back on track.

What has your experience with these or other code generation tools been like? Let me know in the comments!


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
