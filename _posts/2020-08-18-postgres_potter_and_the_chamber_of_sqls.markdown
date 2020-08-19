---
layout: post
title:      "Postgres Potter and the Chamber of SQLs"
date:       2020-08-19 00:49:24 +0000
permalink:  postgres_potter_and_the_chamber_of_sqls
---




When I was a kid in the mid 80's my mom worked at this big corporation in a skyscraper downtown chicago. There was a programmer there called a Wizard who I would annoy on Saturdays. My mom worked and I ran amok in the mostly empty Equitable Building.  "If you want to be a shot caller in my world, be a DBA kid, don't be a programmer like me."

I had no idea what those words meant then but I think i know now. The culture in the 80's was such that a programmer went to the database admin and said "I'm doing this" and the dba made the decision about what database to use and schema and that was where the decision making process was. These days however it's a different atmosphere and programmers are making more decisions than ever, and one of those decisions that many are making is to use PostgreSQL.

<img src="https://i.imgur.com/1XxOio5.png" width="80%"/>

The child of James and  Potter, a young Postgres became the chosen one when he-who-shall-not-be-named.....I’m just kidding, it's not that dramatic. He shall be named and his name was Michael Stonebraker. He had led the team for the predecessor to Postgres(see the pattern?) and started working on the post- database in 1985. Postgres was born and would be called so until the late 90's when it was renamed PostgreSQL.

Everyone talks about the magic of Rails, Ruby, and ActiveRecord, but they are only half right. Rails is like that magic object, imbued with spells and effects you can invoke with a few simple commands "rails g expelliarmus!" and suddenly a bunch of things are moving about. ActiveRecord literally writes spells—SQL queries—for you. But if these are the magic items then surely PostgreSQL is a different type of magic, a deeper, more ancient magic, the kind that once you learn it it will enhance all your Rails magic 10 fold! 

<img src="https://i.imgur.com/VUubCNz.png" width="80%"/>

If you look at many lists of the best databases, you will find PostgreSQL on there. Let’s talk about some of the reasons. 

### Open Source
PostgreSQL is fully open source and free, but not only is it open sourced, the project isn't owned by anyone. PostgreSQL is maintained by an association of volunteer programmers and companies who contribute to the project, reloading new updates yearly, in the second half of the year.
PostgreSQL has some amazing features. Being the most SQL2016 compliant db out there, PostgreSQL supports 160 of the 179 mandatory features for core conformance. This compliance makes it easy to migrate to and from PostgreSQL and other SQL compliant databases.  

### Data Types
PostgreSQL has an amazing array of data types right out of the box. Just a glance at the docs shows 19 different type categories, with sub types in those categories. Using as many of them as I can in my career has become a personal goal. Have you seen the Range type?  Not only that, PostgreSQL allows you to dynamically create your own custom types! 


### Universally Available(mostly)
PostgreSQL is available on just about any platform you can imagine, Linux, BSD, Windows, macOS, even Solaris! 

### How cool is this?
With PostgreSQL you’ll find everything you need in a database. With native JSON support, plenty of ways to extend the functionality, and even the ability to link to external tables on other databases, PostgreSQL has a spell for any type of magic you want to cast.

I’ve just touched the tip of the iceberg here, and I don’t know about you but the idea of such magic out there makes me want to become a wizard, casting SQL queries like a flurry of spells, weaving the web of data to support my applications.  

<img src="https://i.imgur.com/iQZ5qJs.jpg" width="80%"/>

That’s all I have for now, stay safe and keep coding!


