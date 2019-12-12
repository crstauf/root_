# Code Reviews

Performing a code review is both an art and a science: there are critical issues (ex: performance, user experience) and general improvements (ex: code readability and maintainability). The art is going to be, in most cases, left up to the lead developer on the project, but the science, that's going to be pretty much the same.

## Common topics
_(Things to look for)_

- performance issues, and opportunities to improve
- adherence to [code design standards](../code-design) for the team/project
- opportunities to improve code readability and maintability
- logic inaccuracies (incorrect `if` clauses)
- defining of unused variables or properties, and orphaned files
- improper use of elements (`a` vs. `button`, `div` vs. `span`)
- unoptimized assets (images, fonts, CSS, JS)
- chaotic or inaccurate file names
- inline documentation missing or inaccurate
- commented code (not inline documentation)
- inappropriate or ambiguous variable names (ex: `$debug` or `$temp`)

## Etiquette and support

Precise, kind, and appropriate language is a major factor in code reviews being well-received. If your team consists of developers of varying experience levels, a block of code that's hard for you to consume may be easy for another developer to consume. Code design standards attempt to solve this problem, but its not going to solve every problem. Its important to keep this in mind while performing code reviews.

A simple strategy is to avoid saying things like "your code" or "you should". Instead, critique the code, not the author: pretend you've no idea who wrote the code, that the code just self-generated itself, and you providing feedback to the code itself. Even though you're commenting on code, there is a person who wrote it (in most cases), so be thoughtful and helpful, not aggressive and impatient.

Providing a link to an external article or resource that provides additional context on why the code should be changed will help the author in understanding what they need to differently. Describing a change to be made without context likely means it'll just happen again: make an effort to help improve the developers on your team, and reducing time spent doing code reviews!

### Read
- https://css-tricks.com/code-review-etiquette/
- https://simpleprogrammer.com/what-makes-code-readable-not-what-you-think/

## Do you understand it?

If as the code reviewer or lead developer on the project, you don't understand a piece of code, bring it to attention. While responsibility may be distributed across a team, by asking a few questions or for an explanation you may uncover an issue before it ever makes it to production; at the very least, an opportunity to improve performance or readability.