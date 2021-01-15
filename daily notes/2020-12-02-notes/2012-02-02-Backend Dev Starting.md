# Back End Dev
Notes from [[2020-12-02]]
- Front end Component vs Back End component?
- SQL Alchemy
	- When to use Raw SQL vs the ORM features
	- Relationships
	- Backref
		- https://docs.sqlalchemy.org/en/14/orm/backref.html
- "Why have flask, why not let the user hit the database"
- Python
	- Python Web Frameworks
		- Flask [^flaskdoc]
		- Flask Signals [^signaldoc]
			- uses Blinker - why, use cases
	- Python Libraries
		- Celery
			- Beat / Periodic Tasks [^celerybeat]
		- Blinker
- Async vs Sync Tasks
- Considerations of Celery Worker vs  Sync
	- Do we care about data now
	- Or can it be async
- Asynchronous Workers
- Endpoints vs Functions
- What are Decorators
	-  Python Decorators
	-  Why use Decorators
	-  Cross-cutting concerns
-  Clean Architexture
	-  Service and Repository
	-  Service
		-  Deals with Entities
	-  Repository
		-  Deals with DAO
		-  Repo is the layer that touches the DB
		-  Is the DAO the same as Repository
	-  DAO vs Entity
		-  DAO to Entity
		-  Entity to DAO
-  Data Base Transactions
	-  Why do we explicitly save instead just saving when we add
		-  Transaction Scope
	

- Links Shared

	- https://docs.celeryproject.org/en/stable/getting-started/introduction.html
	- https://docs.celeryproject.org/en/latest/userguide/periodic-tasks.html

[^flaskdoc]:  [Flask Documentation](https://flask.palletsprojects.com/en/1.1.x/)
[^signaldoc]: [Signals Documentation](https://flask.palletsprojects.com/en/1.1.x/signals/)
[^celerybeat]: Celery - [Periodic Tasks](https://docs.celeryproject.org/en/latest/userguide/periodic-tasks.html)