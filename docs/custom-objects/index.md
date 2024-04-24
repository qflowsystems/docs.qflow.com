---
layout: default
title: Custom Objects
nav_order: 3
has_children: true
has_toc: false
---

# Custom Objects Overview
---

Q-Action is a highly customizable application that varies significantly from environment to environment, in order to accommodate each unique set of business needs.  One place this shows up most clearly is in Custom Objects.

A Custom Object is a group of related data collected into a single object.  For instance, an environment might have an Employee object that contains data such as an employee's name, phone number, and address.  For that matter, an Address might be its own Custom Object, containing data such as street address, city, state, and zip code.  In that way, Custom Objects can be fields on other Custom Objects.

Frequently, a Custom Object will serve as a primary way of grouping and searching for documents in the system.  In our example, many of the documents that get added to the system might be associated with a specific Employee.  Learn more about using Custom Objects in searches [here](Understanding_Search_Filters.htm).

Some Custom Objects might only have one data field, often an ID.  These Custom Objects are set up for values that may get re-used multiple times throughout the system, so that users can choose to select from existing values or create a new value, if they have the permissions to do so.  This way, single-field Custom Objects provide more structure than [Free-Text fields](Using_Free-Text_Filters.htm) do, while also providing more flexibility than a [List of Values](Types_of_Search_Filters.htm).

Using Custom Objects as fields on Documents, Folders, or other Custom Objects, helps cut down on typos and the need for users to input (and re-input!) data manually.  When, for example, multiple documents should be associated with an Employee named, say, Jane Doe, then you can rest assured that none of those documents are going to end up accidentally associated with non-Employee Jsne Doe, since users must select an existing Employee to add to the Document.

Another way to think of Custom Objects is that they are like lookup tables in a database.  Each type of Custom Object (also called a Custom Object Definition) is its own database table, with each field on the Custom Object a Column, and each instance of a Custom Object (e.g., an Employee like Jane Doe) one row of data.  

