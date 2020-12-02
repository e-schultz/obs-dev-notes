---
tags: ["#DRAFT"]
---

I've worked in tech for over a decade, my most recent experience had been five years at Rangle, focused on full stack Java Script, and more on the Software Engineering side.

While I have had to work with complex data before, and have worked with Data Engineers - so I had a general idea of the problem space, what they did, etc -  but I didn't really know the specifics.

I knew enough to know that I probably had blind spots.

## My TL;DR Understanding

- They build and support the tools/infrastructure to get data from Point A to point B in a fast and efficient way
- Handle data from multiple sources
- Gets it into a format that is appropriate for how it's being used 

Usually as an application scales, and their data needs increase, how you store the data for an appication, is often not the best way to store it for reporting and analytic needs.

- How you write data can be different than how you query data

Being able to take in real time data from other sources, and changes within the transactional database of your application - and get that into a data warehouse that is optimized for analytics and reporting is important.

So, with these broad strokes in mind I started do my searching on [[What is a Data Engineer]]

## The Industry 

Maybe "The Industry" is a bit of a misnomer here - it's to clarify my understanding, and to also better understand the the how, and the value of the role. 

### The How

This is where I wanted to better understand the common skills and tools used by Data Engineers.

1. Step 1 - Collect Data
2. Step 2 - ??????
3. Step 3 - Profit

### [[ETL]]

While I was reading Robert Chang explain [[ETL]] in [[S- 2018 A Beginner’s Guide to Data Engineering — Part I|A Beginner’s Guide to Data Engineering — Part I]], he also talks about consideraions when choosing ETL Frameworks

- Configuration
- UI, Monitoring, Alerts
- Backfilling

He then talks about something that I didn't even consider - that there are two different paradigms for ETL [^1]

- [[SQL-Centric ETL]]
- [[JVM-Centric ETL]]

It didn't even occur to me that SQL vs JVM could be a consideration, and I didn't know if we had a preference for it - or if that would be something we'd be expecting the person to bring with them / influence.

So later on when I was having a meeting with my manager to ensure [[Do me and my Manager share the same expectations|we shared the same expectations]], one of the questions I asked is if we had a preference for one or the other?

Then depending on that

- Do the skills / tools/ technologies  we list in the Job Posting reflect that?
- How do those skills fit within our current engineering culture?




[^1]: [[S- 2018 A Beginner’s Guide to Data Engineering — Part I#Two Paradigms SQL- v s JVM-Centric ETL]]