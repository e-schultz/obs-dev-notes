---
aliases: A Beginner’s Guide to Data Engineering — Part I
---
- #source https://medium.com/@rchang/a-beginners-guide-to-data-engineering-part-i-4227c5c457d7
- #author Robert Chang
-

# Highlights

> Among the many valuable things that data engineers do, one of their highly sought-after skills is the ==ability to design, build, and maintain data warehouses==.

## Two Paradigms: SQL- v.s. JVM-Centric ETL
As we can see from the above, different companies might pick drastically different tools and frameworks for building ETLs, and it can be a very confusing to decide which tools to invest in as a new data scientist.

This was certainly the case for me: At Washington Post Labs, ETLs were mostly scheduled primitively in Cron and jobs are organized as Vertica scripts. At Twitter, ETL jobs were built in Pig whereas nowadays they are all written in Scalding, scheduled by Twitter’s own orchestration engine. At Airbnb, data pipelines are mostly written in Hive using Airflow.

During my first few years working as a data scientist, I pretty much followed what my organizations picked and take them as given. ==It was not until much later when I came across Josh Will’s talk did I realize there are typically two ETL paradigms==, and I actually think data scientists should think very hard about which paradigm they prefer before joining a company.

##

- JVM-centric ETL is typically built in a JVM-based language (like Java or Scala). Engineering data pipelines in these JVM languages often involves thinking data transformation in a more imperative manner, e.g. in terms of key-value pairs. Writing User Defined Functions (UDFs) are less painful because one does not need to write them in a different language, and testing jobs can be easier for the same reason. This paradigm is quite popular among engineers.
- SQL-centric ETL is typically built in languages like SQL, Presto, or Hive. ETL jobs are often defined in a declarative way, and almost everything centers around SQL and tables. Writing UDFs sometimes is troublesome because one has to write it in a different language (e.g. Java or Python), and testing can be a lot more challenging due to this. This paradigm is popular among data scientists.