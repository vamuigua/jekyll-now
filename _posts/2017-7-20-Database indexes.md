---
layout: post
title: DATABASE INDEXES
---

## Defination

A *Database index* is a data structure in the database which improves the speed of operations (typically row lookups) on a database table, or across tables.

Its like using the Content Index in books or even the Bible. When you want to look for a Chapter, you just check the page number from the content index and flip through instantlly without wasting time on going throught each page.
Simple...Right!😃

Well that’s basically how database indexes work. Assuming you have an indexed users.id column on your users table, when you query a database with…

```
SELECT name FROM users WHERE id = 1
```

…the database can find that row very quickly, rather than having to scan through every row in the table and check whether it’s “id” value is equal to 1.

## What should you Index?

### Primary Keys

Most SQL databases with the concept of a primary key will automatically create an index on the primary key column when it exists. In Rails, this is typically the “id” column in a table, and because Rails tells the DB that it’s a primary key, you’ll get the index “for free”, created by the database. This is very important for a “show view” like /users/1, for example. The request comes in, and the query to “find user with id equal to 1” occurs very quickly because the users.id column is indexed.

### Foreign Keys

Now what if that user has_many comments? In Rails, you most likely have a user_id column in your comments table, which the Comment model will use to determine the user that it belongs to. You should have an index on every foreign key column. When you make a page like /users/1/comments, two things need to happen. First, we lookup the user with id equal to 1. Assuming we’ve indexed primary keys, this will be fast. Second, we want to find all comments that belong to this user. If we’ve indexed comments.user_id, this will be fast too.

### Columns used by to_param

Let’s say you’ve got indexes in place on users.id and comments.user_id, but then a request comes in to make “pretty urls” on these pages. Ok, no problem. We add a users.keyword column to users, and allow users to specify a username with their account. Now we can make requests to urls like /users/matt/comments, and see all comments by that user. Well, same situation as before, we need to do a find, but this time we’re matching against the ‘keyword’ column and not the ‘id’ column, so this needs to be indexed.

##Others include:

* Composite keys on join models
* State columns
* Boolean Columns
* Date columns
* Columns used in polymorphic conditional joins
* Columns used in validations
* Columns used for STI
