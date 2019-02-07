---
title: Get Binary Interactions
keywords: engage, about
tags: [development]
sidebar: overview_sidebar
permalink: solution_getbinaryretrieval_interactions.html
summary: Get Binary interactions
---

{% include important.html content="This site is under active development by NHS Digital and is intended to provide all the technical resources you need to successfully develop the NRLS API. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}


## Interactions ##

The API uses the ‘Get Binary Retrieval Pattern’ to support retrieval of non-structured documents such as a PDFs from remote systems.

There are three main systems that need to integrate in order for systems to share data.


| System | Role in Get Structured Document solution | 
|-----------|----------------|
|Consumer|A system that wishes to retrieve an unstructured document to support patient healthcare.|
|Provider|A system that exposes records (unstructured document) for sharing (retrieval).|
|Spine Security Proxy (SSP)|The Spine Security Proxy can facilitate retrieval of unstructured documents [TBC].|


### Consumer System ###

A Consumer system can only read unstructured documents from Providers. A Provider allows a Consumer to retrieve an unstructured document to support patient healthcare.

### Provider System ###

A Provider system is responsible for exposing its records for sharing with Consumer systems. It controls the format of and the way a record can be retrieved. This API limits shared records to “non-structured” document format.


<img src="images/solution/GetBinaryRetrievalRequest_Diagram.png" style="width:100%;max-width: 100%;">

