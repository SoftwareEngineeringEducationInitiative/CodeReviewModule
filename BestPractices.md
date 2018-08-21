# Best Practices for Code Review

- Identify defects, don't attempt to solve them (some advice may be ok, but discuss in detail offline)
- Ask leading questions if the code 'smells' funny ("why did you do it this way?" or "I'm trying to understand this code, walk me through the options you considered" rather than, "why didn't you do it the way I would have?" )
- Ask others (not the author) if they think the code is ok, ask them why they think it is good.
- Ask if this is the best solution, then discuss some options the author can consider for achieving a better solution. The goal of this expensive activity is to ensure the team is creating the best code.
- Think about others who will have to extend the code long after the author is gone. Is the code documented well enough for someone to easily understand it.
- Don't make it personal. Speak to others about their code the way you would like others to speak to you about yours. You must provide constructive criticism.
- Whether you are the author or not, this is a learning experience. Pay attention to what other people are saying. Ask questions!
- Strive for clarity and simplicity. Again, this isn't about "is this correct" (hopefully there are tests and those that demonstrate it works in at least most cases). 
- Even if the code works, is it working *well*? Are you adding new calls to deprecated APIs? Are you calling the outdated/dangerous versions of functions? Are you depending on things that may change in the future?
- Efficiency. Are there hidden O(n^2) (or worse) algorithms? Are the data structures that are being used appropriate?
- Pay *very* close attention to new *types* that are introduced, somewhat close attention to new functions/methods that are introduced, especially if the intent is for those to be used throughout the project. One others are depending on a type or a function, it's much harder to change it.  (See Hyrum's Law http://www.hyrumslaw.com/)
- Are we changing an API, or a behavior of an existing interface? If so, are we sure we know that is safe?  How are we sure? 
- It's pretty useful when code review is done by citation by default - if it's not about the logic of the code in question (and that is a minority of the time in practice), it's good to include citation. Have an agreed-upon style guide, cite that. Cite published (and agreed-upon) best practices. When no citation is available, be clear whether the comment in question is "You must do this, even though I can't show why" vs. "I'd do it this way" or "Have you considered a different way?"
