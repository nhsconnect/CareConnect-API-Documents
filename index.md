---
title: Introduction to the Care Connect Documents API
keywords: homepage
tags: [overview]
sidebar: overview_sidebar
permalink: index.html
toc: false
summary: Overviews Care Connect Documents API FHIR resources and Conformance
---

{% include important.html content="This site is under active development by NHS Digital in collaboration with INTEROPen and is intended to provide all the technical resources you need to successfully develop the Care Connect Documents API. This project is being developed using an agile methodology so iterative updates to content will be added on a regular basis." %}

# Introduction #

<!--
This is the Care Connect Get Unstructured Document RESTful FHIR STU3 ‘Read Only’ experimental API implementation guide. It is a component specification of the Care Connect API (CCAPI) suite. 
-->

The Care Connect APIs have been developed by NHS Digital in collaboration with the INTEROPen community. These APIs aim to  better support the delivery of care by opening up information and data held across different clinical care settings through the use of nationally defined <!--INTEROPen--> FHIR® resources.
<!--
The Care Connect RESTful APIs have been developed collaboratively by NHS Digital and the INTEROPen community. These APIs aim to  better support the delivery of care by opening up information and data held across different clinical care settings through the use of nationally defined INTEROPen FHIR® resources.
-->

{% include note.html content="The Care Connect APIs are based on FHIR STU3 and define the minimum conformance requirements and standards for retrieving patient data and records.<br><br>To learn more about NHS Digital and INTEROPen please refer to the information at the bottom of this page." %}



# Care Connect Documents API #

The Care Connect Documents API RESTful FHIR STU3 Implementation Guide is a component of the Care Connect API specification suite. 

<!--The initial core API has been created to provide read only access to fine grained information represented in FHIR resources.-->

The resources in scope for this API are:



<table style="min-width:100%;width:100%">
<tr id="conformance">
<th style="width:33%;">Foundation</th>
<th style="width:33%;"></th>
<th style="width:33%;"></th>
</tr>
<tr id="conformanced">
<th>Other</th>
<th></th>
<th>&nbsp;</th>
</tr>
<tr>
<td><a href="api_documents_binary.html">Binary</a></td>
<td></td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td></td>
<td>&nbsp;</td>
</tr>
</table>




<!--
-	AllergyIntolerance
-	Condition
-	Encounter
-	Immunization
-	Location
-	Medication
-	MedicationRequest
-	MedicationStatement
-	Observation
-	Organization
-	Patient
-	Practitioner
-	PractitionerRole
-	Procedure
-->

<!--
# API Query Mechanism and Conformance #

The API intends to mandate a minimal set of the query mechanism to ensure the maximum number of systems can implement the API.

 Query parameters conformance will be categorised as:

- <b>MUST</b> – these search parameters MUST be implemented for the specified resource type
- <b>SHOULD</b> – these search parameters are expected to be implemented, if the data to support the query is present in the host system

Additional search parameters can be added to reflect local requirements.

To be conformant, provider systems are required to implement all of the MUST parameters.

All search parameters must be described in the FHIR CapabilityStatement.
-->


<!--

# Using this guide #

This guide has been created to support the adoption of the "your project here" profiles and FHIR resources. As such the site is structured around stakeholders including API users, developers and architects, who have an interest in implementing the "your project here"

Need to add include here....

-->

# NHS Digital #

[NHS Digital](https://digital.nhs.uk/) is the national information and technology partner to the health and care system using digital technology to transform the NHS and social care.

To learn more about the Interoperability efforts at the NHS Digital, visit the [NHS Digital Interoperability](https://www.england.nhs.uk/digitaltechnology/connecteddigitalsystems/interoperability/) pages.


# INTEROPen #

INTEROPen is an OPEN collaboration of individuals, industry, standards organisations and health and care providers, who have agreed to work together to accelerate the development of open standards for interoperability in the health and social care sector.

The INTEROPen vision is to create a library of nationally defined HL7® FHIR® resources and interaction patterns that implementers can adopt to simplify integration and interoperability within UK health and social care.

Find out more on the [INTEROPen website](http://interopen.org/).