---
aliases: medallion architecture 
---

I haden't heard the term medallion architecture before, but as she was explaining it - it made sense. 

Going from the raw data, then creating the bronze, then silver, then gold data - and it getting more refined along the way, and the processes around that.

- [Data Quality Testing in the Medallion Architecture with Pytest and PySpark](https://www.youtube.com/watch?v=mZ33PJzJtlw)


> ![[kafka data quality Pasted image 20201215220220.png]]
>
>- Bronze: the initial landing zone for the pipeline. We recommend copying data that’s as close to its raw form as possible to easily replay the whole pipeline from the beginning, if needed
> - Silver: the raw data get cleansed (think data quality checks), transformed and potentially enriched with external data sets
>- Gold: production-grade data that your entire company can rely on for business intelligence, descriptive statistics, and data science / machine learning
> Following our own medallion architecture, we break it out as follows for our audit logs ETL design: [^1]

https://databricks.com/notebooks/Audit-Logs-ETL.html


[^1]: [Monitor Your Databricks Workspace with Audit Logs](https://databricks.com/blog/2020/06/02/monitor-your-databricks-workspace-with-audit-logs.html)