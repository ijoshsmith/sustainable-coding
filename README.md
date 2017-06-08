# Sustainable Coding

> We are what we repeatedly do. Excellence, then, is not an act but a habit. - Aristotle

This document describes my ever-evolving perspective on the strive for excellence as a software developer. Its focus is on writing code, more than code itself. Even though creation and the thing created are intimately related, I consider improvements made in a software developer's mindset to be more important than improvements made in a source code file.

I chose the title 'Sustainable Coding' to reflect this ambition. Here's why…

**Sustainable**

Despite the current buzzword status of *sustainable* I could not find a better adjective to describe my objective. Two definitions of [sustainable](http://www.oxforddictionaries.com/us/definition/american_english/sustainable) from Oxford Dictionary are:
- Able to be maintained at a certain rate or level
- Able to be upheld or defended

These definitions provide the raw material for a professional software developer's creed: 

> I develop high-quality software that can be maintained at a reliable rate, using only practices which I am willing to uphold and defend.

**Coding**

I chose *coding* instead of *code* as the second word of the title to emphasize my focus on writing code more than the code that is written. It might be a subtle distinction, but it is an important one.

## APE
When working on something, resist the temptation to jump directly into writing or changing code.

It is important to Assess, Plan, and Execute (APE).

- Assess the requirements, problems, unknowns, etc.
- Plan how to implement the work that needs to be done, based on your assessment.
- Execute your plan.

> The first casualty of any battle is the plan of attack. - Cory Doctorow

It's common to go back to assessment or planning as new facts are uncovered.

## Fixing bugs
Give each bug fix its due diligence, otherwise your fix will likely create more bugs.

Fix the problem, not a symptom.

Decide how to fix a bug only once you understand what causes it.

If you can't explain why your fix works, it is not a valid fix.

## Writing for the reader
### Readability
Code should be written so that it is easy to read.

The easier code is to read, the less difficult it is to maintain and extend.

A subjective measure of how easily code can be read is called "readability."

Consistently applied code formatting and naming conventions improve readability.

The choice of particular formatting and naming conventions is far less important than their consistent usage.

### Signal-to-noise ratio

![Signal in the noise](/images/signal-to-noise.png)

An empty source code file has no "visual noise."

Every character of text added to a file increases its visual noise.

The developer's intent is a "signal" which someone reading the code discovers in the visual noise.

Maximizing readability involves finding a signal-to-noise "ratio" that conveys your intent, without obscuring it with too little or too much text.

For example, a local variable that is only used in a short block of code should not have a long name. Similarly, the name of a function or class used by other modules should not be terse or abbreviated.

Another way to improve the signal-to-noise ratio is to ensure that every character of text is necessary. A line of code that is unnecessary, or unnecessarily complicated, increases the amount of visual noise while decreasing the signal strength.

## Choosing names
### Call it what it is
The name of a thing determines what you think that thing is. 

A poorly chosen name distorts your understanding of what a thing is.

When understanding is distorted by a name, a "mental mapping" is needed to bridge the gap.

Mental mappings increase the reader's cognitive burden, thereby decreasing their ability to effectively work with and improve the codebase.

Rename something if its role/purpose changes. Don't stick with the old name because you happen to know what it currently means. Other developers (including Future You) will need to spend time and energy creating a mental mapping.

### Select your words as carefully as a lawyer
A name should make it clear what something is or does, not how it is implemented.
- Prefer: `findHighestPaidEmployee()`
- Avoid: `selectFirstEmployeeFromListSortedBySalary()`

Specific, accurate names have better explanatory power:
- Prefer: `authenticateUserIfRequiredAfterProlongedInactivity()`
- Avoid: `authenticateUserIfRequiredByTheRules()`

Suppose you need to write a method that modifies a customer's `Priority` based on a `Status` field. 
- Good name: `adjustCustomerPriorityBasedOnStatus()`
- Poor name: `makeCustomerPriorityMatchStatus()` 
- Rationale: The customer's `Priority` and `Status` fields are related but not equivalent or *matching*. Therefore, the word "match" in the second example is inappropriate and misleading.

### Avoid creating junk drawers
![Junk drawer](images/junk-drawer.png)

Vague class names, like `SessionManager` or `DataController`, should be avoided because such classes tend to become a junk drawer whose existence discourages developers from critically analyzing where to put new code. 

Junk drawer classes are large, disjointed, and complicated. This makes them difficult to understand and fix.

As more and more code accumulates in a junk drawer, it becomes difficult to *not* put new code into it, because it contains so many things that need to be referenced.

## Improving code in a business workplace
> It's easier to ask forgiveness than it is to get permission. - Grace Hopper

Code can, and should, be improved.

Improvements can be categorized as "external" or "internal."

External improvements increase the value of software for users.

Internal improvements increase the livability of a project for developers.

Fixing a bug is a type of external improvement.

Removing knowledge duplication is a type of internal improvement.

In a business workplace, internal improvements sometimes must be made "under the radar" because non-developers seldom appreciate the importance of changes that have no immediate impact on scheduled deliverables. 

As a professional software developer it is your duty to make frequent, minor internal improvements to a codebase, despite the opinions of non-technical managers unqualified to appreciate the psychological benefits such changes can have for developers. 

A professional software developer should not, nor should be required to, ask management for permission to make minor internal improvements. 

On the other hand, it is unprofessional to covertly spend a lot of time making broad, sweeping changes in order to implement an internal improvement. Such changes can introduce unnecessary risk and take too much time away from making business-critical external improvements.

Strike a balance between doing what your employer tells you is necessary and doing what you know is best for your team, based on your expertise as a professional software developer.

---

*This is a continual work-in-progress. More to come…*
