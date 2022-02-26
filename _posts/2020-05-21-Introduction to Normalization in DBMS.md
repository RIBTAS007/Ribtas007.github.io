---
layout: post
title: "Introduction to Database Normal Forms"
description: In this article I will try to give you a brief update regarding normalization in DBMS.
image: /files/blogs/normalization/normalization.png
date: 2020-05-21
categories: post
tags: [Database, Normalization]
---

## Abstract

Normalization is a process of minimizing redundancy from a relation. There are various forms of redundancies like 1NF, 2NF, 3NF, and BCNF that minimize redundancy. 
Scope

*	This article covers a brief overview of Normalization and its various forms like 1NF, 2NF, 3NF, and BCNF.
*	It does not discuss about how we can convert a given relation to these normal forms.

## Contents

*	What is Normalization, and why do we use it ?
*	1 NF
*	2 NF
*	3 NF
*	BCNF
*	Summary

## What is Normalization, and why do we use it?

Consider the student table below that contains the details about the marks scored by students in Physics subject in class 10th which was taught by Arjun Sir. 

|Roll Number  |	Name        |Score	     |Class        |Subject	    |Teacher Name |
| ----------- | ----------- |----------- | ----------- |----------- | ----------- |
| 1	          |Abhimanyu	|90	         |10	       |Physics	    |Arjun        |
| 2	          |Pragy	    |70	         |10	       |Physics     |Arjun        |
| 3	          |Vidushi	    |75	         |10	       |Physics     |Arjun        |
| 4	          |Satbir	    |61	         |10	       |Physics	    |Arjun        |
| 5	          |Simran	    |89	         |10	       |Physics	    |Arjun        |
| 6	          |Pushti	    |88	         |10	       |Physics	    |Arjun        |

**Table 1: Student info**

Each row in the table is called a record, and each column denotes an attribute. We can see that the “Class”, “Subject”, and “Teacher Name” attributes have the same values for all the records. These values are repeated unnecessarily multiple times in the Database and thus are creating redundancy. Redundancy is mainly caused when we need to store the same values repeatedly in our Database.

If we want to add a record in the table, we need to store the same values, i.e., <10, Physics, Arjun>. Similarly, if we want to update the “Teacher Name” corresponding to the Physics subject in the records, we need to update each record. Thus having redundancy in a relation is a waste of space as well as time. It causes various issues while inserting, updating, and modifying the database records. 

To resolve this issue of having redundancy in a database, we use the concept of Normalization. Normalization mainly aims to create a separate table for each entity present in our Database. For example, if we observe the table, we can see that we mainly talk about two things or entities. The first entity is a “Student”, and the second entity is the “Subject” that s/he has taken. Hence, by making a separate table for each entity, as shown below, the redundancy can be reduced a lot.

|Subject_ID|	Class	|Subject|	Teacher Name|
| ----------- | ----------- |----------- | ----------- |
|PY	|10	|Physics	|Arjun|
 
 
|Roll Number  |	Name	    |Score       |	Subject_ID|
| ----------- | ----------- |----------- | ----------- | 
|1	|Abhimanyu	|90	|PY|
|2	|Pragy	    |70	|PY|
|3	|Vidushi	|75	|PY|
|4	|Satbir	    |61	|PY|
|5	|Simran	    |89	|PY|
|6	|Pushti	    |88	|PY|

**Normalization** is a process of removing redundancy from a database and improving its structure to minimize issues related to insertion, deletion, or updating of data. There are various forms of Normalization which we will discuss in the next section. 

## 1 NF

To check whether a table is in first normal form(1NF) or not, we should take care of the following points:
*	Every cell in the table should have a single value or atomic value.
*	Every attribute(column) should have the same type(domain) of value. 
*	Every attribute(column) should have a unique name.
*	The order of attributes(columns) and records(rows) do not matter. Any attribute(column) can be placed anywhere in the table. Any record(row) can be set anywhere in the table.
If a table or relation follows all the above conditions, we can say that the relation is in 1NF. 

## 2 NF

“*A relation is said to be in second normal form(2NF) if it does not have a partial dependency and is also in first normal form(1NF).*” 

In order to understand partial dependency, let us first know some basic terminologies with the help of an example. 

Consider a relation(table) having four attributes, P, Q, R, S having the following dependencies:
*	P, Q -> S
*	Q -> R

Using P and Q, we can derive S, and using only Q, we can derive R. Hence, we can say that if we use both P and Q together, then we can derive all the attributes of the table, i.e., P, Q, R, S. (since P -> P and Q -> Q is self-explanatory). 

We can write as (PQ)+ = {P, Q, R, S}, or in simple words, we can say the closure of P and Q gives us all the attributes of the relation. The minimal sets like PQ in a relation(table) that are capable of deriving all the attributes of a relation(table) are called Candidate keys. There can be more than one candidate key in a table. 

If an attribute is a part of any candidate key of the relation, then it is called a Primary attribute else, it is said to be a Non-Primary attribute. In the example above, we can say that P and Q are primary attributes, and R and S are non-primary attributes.

We now know the basic definitions required to understand the concept of partial dependency. In the above example, S is dependent on all the primary attributes, i.e., P and Q. If either P or Q are missing, then we cannot derive S. In the case of R, it is not the same. Even if P, a primary attribute, is missing, we can still derive R using only Q. Hence, instead of depending totally on the candidate key, R is partially dependent on Q, part of a candidate key. This is the concept of partial dependency. 

If a non-primary attribute is dependent only on a part of the candidate key, i.e., a prime attribute and not on the whole candidate key, then the relation(table) has a partial dependency. 

Hence a 2NF can have the following kind of dependency
* Non-Prime -> Prime
* Non-Prime -> Non-Prime
* Candidate Key -> Prime
* Candidate Key -> Non-Prime

but it cannot have a partial dependency, i.e.,  Prime -> Non-Prime

## 3 NF

“*A relation is said to be in third normal form(2NF) if it does not have a transitive dependency and is also in second normal form(2NF).*” 

Let us understand the concept of transitive dependency with the help of an example. 

Consider a relation(table) having four attributes(columns) P, Q, R, S having the following dependencies:
*	P, Q -> R
*	R -> S
*	
Here, P and Q together are deriving R, and R is further deriving S. Hence P and Q can determine all the attributes of the table, i.e., (PQ)+ = {P, Q, R, S}. Therefore, PQ is a candidate key in the table. Also, PQ is not deriving S directly. It is deriving S with the help of R. This is what we can call a transitive dependency.

When we have a dependency present in a table such that a non-prime attribute is dependent only on another non-prime attribute(s), the relation is said to have a transitive dependency. 

Hence a 3NF can have the following kind of dependency
* Non-Prime -> Prime
* Candidate Key -> Prime
* Candidate Key -> Non-Prime
* but it cannot have a partial dependency and transitive dependency, i.e., 
  * Non-Prime -> Non-Prime (transitive dependency)
  * Prime -> Non-Prime (Partial Dependency)
  
## BCNF

A super key can be defined as a set of attributes that can determine all the attributes in a given relation. A super key with a minimal number of attributes is called a candidate key.

A relation is said to be in BCNF only if it contains the following kind of dependency:
* Super Key -> Prime
* Super Key -> Non-Prime

It cannot have the following dependencies:
* Non-Prime -> Non-Prime (transitive dependency)
* Prime -> Non-Prime (Partial Dependency)
* Non-Prime -> Prime
* Prime -> Prime

## Summary

*	Normalization is used to minimize the redundancy in a database. There are various forms of Normalization. 
*	1NF mainly deals with having atomic values in every cell and ordering of attributes and records. 
*	2NF deals with partial dependency. 
*	3NF deals with transitive dependency 
*	BCNF only allows attributes to depend on the super key.




