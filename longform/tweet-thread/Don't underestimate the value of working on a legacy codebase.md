# Don't underestimate the value of working on a legacy codebase 
- via [[@ep82]] - [twitter](https://twitter.com/e_p82/status/1154360318635782144)

Don't underestimate the value of working on a legacy codebase that might look like a bit of a mess at first glance. 

Some of my biggest growth moments as a developer came from learning how to debug, reproduce problems, refactoring and adding new features in legacy systems.

# Copy Paste Architecture

Working on an  ASP.NET WebForm application - "just copy this folder and change the name space to be v3".

No separation of concerns, everything mashed into the code-behind. 

So much copy-paste/repeated code.

## Overtime: 

**Refactoring into Layers**
- refactoring things into a business logic layer, data access/repository library
- refactored to a WCF service, initially meant for 'internal API' for various apps 
- that was then used for a fresh version using .NET MVC

**Transition from "We have an API" to "We have an Internet Friendly API"**

We then considered what would a web-friendly API actually look like next.

- Then got a WebAPI layer built on top to make a public API for it
- That started to drive SPAs, mobile versions, workflows, etc
- Then some of the components  built that were consuming the API's - started to get used within the initial WebForm apps that we still maintained

That's not even touching on the desktop applications we had, or the workflow services, or our own custom task/workflow runner/scheduler. 

## INTEGRATION'S 
Or needing to integrate with clients 3rd party systems - and getting massive data dumps in the form of a CSV file uploaded daily.

- "How do we know that a contractor was terminated?"
- "They don't appear in that CSV file anymore" 
- "Can't we get a list of people terminated?" 
- "No"
- "Why not?" 
- "Reasons..."

But, if there was an extension request - needing to trigger another flow.

That extension request may get entered in late, or at times get rejected. 

At times it was just that the contract ended - and they weren't fired.

Other times it was an early termination, which could be triggered from numerous places.

I learned a lot over the years working on that system, I was still wrapping up my last year in school at night school when I started that job.

If it had been a perfectly architected, modern, greenfield system - I don't think I would have learned as much as I did.

Feeling the pain points helped me better understand the "why" behind some things, and how I approach them now.

- [[Learn how to debug]] such a complex system was an invaluable skill.
- How to do large scale refactoring - but incremental and over time.
- Build Sandbox applications 


Out of necessity - learning how to build sandbox applications that consumed different api's / libraries / etc to try and reproduce bugs, test out new ideas without needing the entire solution.

## Sometimes ask What not How

![[Sometimes ask What not How]]
