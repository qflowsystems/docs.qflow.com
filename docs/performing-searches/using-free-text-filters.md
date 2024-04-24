---
layout: default
title: Using Free-Text Filters
nav_order: 5
parent: Performing Searches
---
# Using Free-Text Filters
{:.no_toc}
---
Free-Text filters such as Document Title and Document Content allow you to use special syntax to construct more specific searches.  To demonstrate the options we will search for a document that contains the following sentence: _The quick brown fox jumped over the lazy dog._
- TOC
{:toc}

## Simple word search
To search for documents containing a single term, simply enter the term into the search field.

## Wildcards
Wildcard searches can be performed by placing an asterisk or question mark in the search term. 

An asterisk will match on zero or more characters.  The query: _jump\*_ would find words that start with the letters "jump" such as jump, jumps, jumping, jumped.

A question mark will match on a single character.  The query: _f?x_ would match on words such as fax, fix, fox.

## Multiple Terms
If more than one term is entered into the field then by default the application searches for content that matches one term or the other.  Consequently, the search: _fox bear_ would return documents containing the word "fox" or the word "bear".

## Phrases
To search on a phrase, the group of words are surrounded by double quotes such as: _"quick brown fox". This would only match content that contains that exact phrase._


## Require/Prohibit Terms
You can use the plus (+) and minus (-) characters to denote that certain terms are "required" or "prohibited". 

The query: _+fox +dog_ will return results that must have both the word "fox" and "dog".

The query: _+fox -dog_ will return results that must have "fox" but must not have "dog".

## Sub-Queries
You can use parenthesis to group terms to form sub-queries. 

The query: _+(dog cat) +fox_ will return results where "dog" or "cat" must be present, and "fox" must be present.

## Fuzzy searches
Fuzzy searches discover terms that are similar to a specified term without necessarily being an exact match. To perform a fuzzy search, use the tilde ~ symbol at the end of a single-word term. 

For example, to search for a term similar in spelling to "roam," use the fuzzy search: roam~

This search will match terms like roams, foam, & foams. It will also match the word "roam" itself.

For those who are curious, these fuzzy searches are based on the Damerau-Levenshtein Distance or Edit Distance algorithm.

## Proximity searches
A proximity search is like a fuzzy search, but specifically looks for terms that are within a given "distance" from one another.  To perform a proximity search, add the tilde character ~ and a numeric value to the end of a search phrase. 

For example, _"quick dog"~_6 would match on the sentence "The quick brown fox jumped over the lazy dog" because there are 6 (or fewer) terms between "quick" and "dog".

The search _"quick dog"~5_ would not match the example sentence because the term distance between "quick" and "dog" is greater than 5.

## Boosting a Term
Boosting a term tells the search engine that you care more about results that match that term than other terms.  

It is important to Sort By Relevance when boosting a term, otherwise the boost has no impact on the search results.

To boost a term use the caret symbol ^ with a boost factor (a number) at the end of the term you are searching. The higher the boost factor, the more relevant the term will be.

Boosting allows you to control the relevance of a document by boosting its term. For example, if you are searching for brown _fox_ and you want the term "fox" to be more relevant, you can boost it by adding the ^ symbol along with the boost factor immediately after the term.

For example: _brown fox^4 w_ill make documents with the term "fox" appear more relevant than documents that only contain "brown".

You can also boost Phrase Terms as in the example:  _"quick brown fox"^4 "lazy dog"_