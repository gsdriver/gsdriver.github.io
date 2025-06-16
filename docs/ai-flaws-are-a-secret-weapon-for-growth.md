# AI’s Flaws are a Secret Weapon for Growth - Here’s Why

### Don't run from AI Hallucinations - use them for growth!

###### *June 16, 2025*

<p align="center">
  <img height="400" alt="Photo by Components AI" src="./images/ai-flaw-hero.jpg">
</p>

Like many, I’ve been using generative AI tools to accelerate my software development. It’s been especially helpful in areas where I have less expertise. Areas where I know enough to mentor for better performance and accuracy, but not enough to complete the task unaided. In the Dunning-Kruger effect, it's where you know enough to know you’re not an expert and are starting the climb towards mastery.

## Hallucinations Are Powerful Accelerants

AI is notorious for hallucinations with many comical examples of incorrect output. Consider this example to retrieve customer orders joining IDs from one table with names from another. Syntactically correct but logically flawed. It can be frustrating when an AI tool insists this is valid when asked to fix it:

```
SELECT customers.name, orders.order_total
FROM customers
JOIN orders ON customers.id = orders.customer_name;
```

It can be annoying to see hallucinations when you are a novice looking for a complex solution. But I’ve come to see these hallucinations as **powerful accelerants** in my own learning. I learn best by doing - picking up a problem and stepping through it. Having a real-word application helps me visualize concepts in a concrete manner. When I know what code should do and see incorrect results, stepping through it is a perfect learning opportunity. I couldn’t do this without experience. But my background lets me understand the logical process. Doing an in-depth code review lets me focus on each step to hone in on the incorrect logic. This gives me a better sense of the approach of the code. It lets me either provide a more detailed prompt to get a correct result, or to make direct changes to the code.

> I've come to see AI hallucinations as *powerful accelerants* in my own learning

## Building SQL Expertise

<p align="center">
  <img height="300" alt="Photo by Fotis Fotopoulos on Unsplash" src="./images/ai-flaw-development.jpg">
</p>

In my latest project, I’m building dynamic dashboards with more complex SQL queries in BigQuery. I'm an intermediate SQL developer, and have tended to rely on JavaScript for more complicated logic rather than pushing SQL to its limits. This project has forced me to refine that approach. For example, I needed to provide order summaries based on some unique criteria. I turned to GitHub Copilot for some code. It generated a query that didn’t work using concepts I was less familiar with such as temporary tables and CASE statements. The problem wasn’t with the syntax, it was with the underlying logic. I could see how these concepts were applied, and got a sense of why the code used them for the problem I was trying to solve.

> The problem wasn't with the code's syntax but with the underlying logic. This was a powerful tool to further my learning

As I worked through the AI-generated SQL, I realized the mistakes weren’t obstacles but invitations to think more critically. Breaking down the AI-generated query step by step helped me pinpoint where the aggregation was failing. Rows were not being de-duplicated before being used in one of the CASE statements, leading to skewed results. By systematically testing each part, I clarified the aggregation error and deepened my understanding of SQL conditional logic at scale. I’m now leveraging CASE statements directly into my SQL to streamline execution while keeping everything within the database layer. Doing conditional aggregations within a single query optimizes execution and the transfer of data.

## Summary

> The best leaders will use AI's imperfections to grow

John F Kennedy said, “Those who dare to fail miserably can achieve greatly.” The strongest developers, and the best leaders, will be those who use AI’s imperfections to refine their thinking, adapt quickly, and push technical boundaries.

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
