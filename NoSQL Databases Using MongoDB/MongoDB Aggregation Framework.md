# Aggregation Framework

## Introduction

- MongoDB is a document-based NoSQL database where data is organized in collections that are made up of JSON documents. As with any database, MongoDB has a language that a user can use to access data. In MongoDB’s case, this language is the MongoDB Query Language or simply, MQL. Whether MQL or SQL, database queries can start off simple, but as a database scales more complex queries arise.
- The MongoDB Aggregation Framework is a way to query documents from MongoDB in a way that breaks down these more confounding queries. It separates complex logic into sequential operations.

## How does the MongoDB Aggregation Framework work?

- The purpose of MongoDB’s Aggregation Framework is to design a pipeline consisting of multiple stages for processing documents. You start with your collection's data and after each stage of the pipeline you are closer to the end result which will be the desired documents.
- Each stage performs an operation on the documents. There are several operations that can be conducted. For example, a stage can filter, group, or even calculate values on the data. After each stage, the outputted documents are passed into the next stage and so on until no stages are left.

## What are the most common MongoDB aggregation operations?

- `$project` : Reshapes each document in the stream, such as by adding new fields or removing existing fields. For each input document, outputs one document.

- `$match` : Filters the document stream to allow only matching documents to pass unmodified into the next pipeline stage. $match uses standard MongoDB queries. For each input document, outputs either one document (a match) or zero documents (no match).

- `$group` : Groups input documents by a specified identifier expression and applies the accumulator expression(s), if specified, to each group. Consumes all input documents and outputs one document per each distinct group. The output documents only contain the identifier field and, if specified, accumulated fields.

- `$sort` : Reorders the document stream by a specified sort key. Only the order changes; the documents remain unmodified. For each input document, outputs one document.

- `$skip` : Skips the first n documents where n is the specified skip number and passes the remaining documents unmodified to the pipeline. For each input document, outputs either zero documents (for the first n documents) or one document (if after the first n documents).

- `$limit` : Passes the first n documents unmodified to the pipeline where n is the specified limit. For each input document, outputs either one document (for the first n documents) or zero documents (after the first n documents).

- `$unwind` : Deconstructs an array field from the input documents to output a document for each element. Each output document replaces the array with an element value. For each input document, outputs n documents where n is the number of array elements and can be zero for an empty array.
- [🔥Mongodb Aggregation Tutorial | Aggregation Functions in Mongodb | Mongodb Tutorial | Simplicode](https://www.youtube.com/live/1s5RLZM8oCU?si=A7aSLDMpwK4qpvTf)
