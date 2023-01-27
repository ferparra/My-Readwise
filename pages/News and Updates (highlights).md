title:: News and Updates (highlights)
author:: [[Mike]]
full-title:: "News and Updates"
category:: #articles
url:: https://www.sqlalchemy.org/blog/2023/01/26/sqlalchemy-2.0.0-released/
tags:: #[[data engineering]] #[[data engineering ]] #[[python]] #[[SQL]]

- Highlights first synced by [[Readwise]] [[Jan 27th, 2023]]
	- SQLAlchemy 2.0 introduces support for an Annotated Declarative mapped class to be generated as a **Python dataclass** directly; this will provide an ORM mapped class declared like any other that features auto-generated dataclasses methods such as __init__(), __repr__(), __eq__(), and all the rest. ([View Highlight](https://read.readwise.io/read/01gqrqtbq6jaagzm6qwasjjc08))
	- **An all-new, fully ORM-integrated approach to bulk INSERT that is typically an order of magnitude faster on most backends** - Most of SQLAlchemy's supported databases and drivers have now added or improved their support for INSERT RETURNING syntax, and SQLAlchemy 2.0 has taken advantage of this by supporting and improving RETURNING support for all of its backends, with the sole exception of MySQL (MySQL only; MariaDB supports RETURNING) ([View Highlight](https://read.readwise.io/read/01gqrqty2gmty48kdcqy7mzd02))