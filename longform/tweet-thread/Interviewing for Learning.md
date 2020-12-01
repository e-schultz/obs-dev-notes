# Interviewing for Learning

## Looking for the lightbulb moment

forrestbrazeal on twitter asked:
![[202011262214 How can you evaluate a skill  like learning]]

Some, say it is impossible - 

![[Learning - great skill, difficult to interview for]]

- Curiosity
- Willingness to be wrong
- Able to explain
- Can introduced to a new idea/concept and see how they could apply the

# Some of the ways I've tried to do this in the past.

> note: This is what I've done - and it's not always right/best, and always room to improve.
>
> If anything here is potentially harmful - I'd like to know, interviews are hard enough as is and I do not want to be accidentally excluding people from the process by unfair practices.

## I try and get to what I consider a bit of a 'lightbulb moment'

Where I can get a sense of where their current knowledge/understanding is at, and then see if I can introduce a concept that is an appropriate stretch for them.

## [[202011262241 Avoid Trick Questions|Avoid Trick Questions]]

![[202011262241 Avoid Trick Questions#^8794f3]]

 

## First - try and get a sense for what they have worked on, and what were they responsible for. 

I use this to try and gauge where they are at - asking someone who had no role in the architecture choices to explain those choices and tradeoffs is not valuable

If they were responsible for the architecture and drove it - ooh, that can be fun to explore more.

### Example - Learning Promises

If through questions and talking about code, I realize that they don't know that: Promises return Promises 

I might write some code, or explain a problem of which making use of Promises returning Promises would be useful.

Once they go through and explain how they would do it, I might then ask:

> "[[Well, what if Promises returned Promises]]?"

The lightbulb moment I look for is that "ooh, ahh... ahah!"

and then it's like I can see them refactoring the last year of code in their head.

#### Teachable Moment

Even if during the interview, it has a "how Promises work" lesson, that is ok - and actually, is exactly what I am looking for.

> "oh cool, I see we can learn something together".

This is NOT about finding a knowledge gap to make them feel small about.

Sometimes it could be a more fundamental concept like functions can return functions. 

Maybe they have been making use of it, but didn't really 'click' - and what that opens up.

Or if it's a more experienced developer - could be more abstract concepts.

Maybe if the stack at their old job didn't have anything with the concept of middle-ware, and they don't know what middle-ware is

Explaining the concept,  - "here is what middle-ware is, here is how it's used in Express, here is how it's used in Redux" --- "considering how you approached X before, how might you use it there?"

If the ask is too big of a jump and starts to feel unfair, I'll then try and carefully scale it back to a more fair ask and keep them feeling comfortable and confident.

This is tricky to do, and takes a pretty personal approach - and it's hard to have a set of questions that fit onto a rubric to get there.

I think that this may be one of the faults of the approach - is that it can be difficult to scale and replicate.

I do think that there is importance in consistency in the interview process, but at the same time I am not a fan of the "ask these exact same questions" - it places too much focus on the interviewer, and not the candidate

Earlier on in my career I have Face with symbols over mouth up this approach and produced some awful interview processes, but hopefully noticed that they wern't working very well and course corrected quickly (maybe I'll tweet about my failed attempts later)

# The TL;DR

I think I can TL;DR this thread to:

If you are interviewing for a learner mindset,  but not willing/able to find the appropriate level of concept to teach them during an interview: 

Your doing it wrong.

Something to also consider - is it might not be a knowledge gap, it could be an incorrect mental model.

This is where the idea of questions that have diagnostic power for a formative assessment.

https://teachtogether.tech/#s:models-formative-assessment

![[S- 2019 - Book - Teaching Tech Together#Common Novice Misconceptions]]


![[Pasted image 20201126223609.png]]
![[Pasted image 20201126223622.png]]
	

Going back to my 'Promise returns a Promise' example.

- Do they not understand Promises?
- Do they not know that you can chain them?
- Do they not understand that functions can return functions?

Maybe it turns out that they don't understand that functions can return functions,

*tech gate-keeper twitter scoffs and says no, no hire*

What I would do - is remove Promises from the equation, and give a mini function return function lesson

Time depending, and if we are having fun - ask questions that would make use of a function returning a function, a 'makeLogger' for example.

If don't understand closures - explore that more - and leave it there

We might not get back to Promises at all, am I looking for the ability to learn, or that they know that Promises return Promises?

They just proved to me that they are a learner, and that I will be able to teach them when I hire them.