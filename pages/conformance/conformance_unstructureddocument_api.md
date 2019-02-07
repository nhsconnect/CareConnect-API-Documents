---
title:  Conformance Overview
keywords: getcarerecord, structured, rest, resource
tags: [conformance]
sidebar: foundations_sidebar
permalink: conformance_unstructureddocument_api.html
summary: "Overview of the Conformance section"
---

{% include custom/search.warnbanner.html %}

<!-- include custom/api_overview.svg -->

<!--## 1. Pre-Requisites for FHIR Servers ##-->

## 1.Care Connect Documents API Conformance Requirements ##

This section outlines conformance requirements for Care Connect Documents API Servers<!--and Client applications-->, identifying FHIR resourcess, RESTful operations and the search parameters to be supported. 

<!--
Note: The individual Care Connect Core profiles identify the structural constraints, terminology bindings and invariants, however, implementers must refer to the conformance requirements for details on the RESTful operations, specific profiles and the search parameters applicable to each of the US Core actors.
-->

### 1.1 Care Connect Documents API Requirements ###

- MUST support HL7 FHIR STU3 version 3.0.1.
- MUST support the Binary resource.
- MUST Implement REST behavior according to the [FHIR specification]({{ site.hl7_baseurl.stu3 }}http://hl7.org/fhir/STU3/http.html){:target="_blank"}
- MUST support XML **or** JSON formats for all CareConnect API interactions and SHOULD support both formats.
- MUST declare a CapabilityStatement identifying the list of resources, operations and search parameters supported.
  - In order to be a compliant FHIR server, Servers <!--client systems--> MUST expose a valid FHIR [CapabilityStatement]({{ site.hl7_baseurl.stu3 }}http://hl7.org/fhir/STU3/capabilitystatement.html){:target="_blank"} instance. See the [capabilities](api_foundation_capability.html) interaction.
  - This MUST conform to the Care Connect Documents API `Requirements` [Capability Statement](examples/CareConnect-Documents-ServerRequirements-CapabilityStatement-1v0.1.xml){:target="_blank"}.

<!--  with the See also the Care Connect [Core API CapabilityStatement Requirements](api_foundation_capability.html) profile. -->


<!-- MUST Implement REST behavior according to the [FHIR specification]({{ site.hl7_baseurl.stu3 }}http.html){:target="_blank"} -->
<!-- MUST support at least one additional resource profile from the list of CareConnect Profiles -->
<!-- Resources MUST identify the CareConnect profile supported as part of the [FHIR Base Resource](https://hl7.org/fhir/STU3/resource-definitions.html#Resource.meta){:target="_blank"}-->
<!--
### 1.2 FHIR Conformance ###

SHALL declare a Conformance identifying the list of profiles, operations, search parameter supported.

In order to be a compliant FHIR server, client systems need to expose a valid FHIR [Capability]({{ site.hl7_baseurl.stu3 }}capabilitystatement.html){:target="_blank"} profile. See also [Care Connect API FHIR Capability profile](api_foundation_capability.html).
-->


### 1.2 Profile Interaction Summary ###

1. All servers MUST make available the <a href="http://hl7.org/fhir/STU3/http.html#read">read </a> and <a href="http://hl7.org/fhir/STU3/http.html#search">search </a> interactions for the Profiles the server chooses to support.

<!-- 2. All servers SHOULD make available the <a href="http://hl7.org/fhir/STU3/http.html#vread">vread </a> and <a href="http://hl7.org/fhir/STU3/http.html#history-instance">history-instance </a> interactions for the Profiles the server chooses to support.-->

<!--
Summary of the Care Connect Core API search criteria

Specific server search capabilities are described in detail in each of the resource sections.




<table style="min-width:100%;width:100%">
<tr id="clinical">
	<th style="width:10%;">Resource Profile</th>
    <th style="width:55%;">Supported Searches</th>
    <th style="width:20%;">Supported Includes</th>
    <th style="width:15%;">Supported Modifiers</th>
</tr>
<tr>
    <td><code class="highlighter-rouge"><a href="api_clinical_allergyintolerance.html">AllergyIntolerance </a></code></td>
    <td>patient, patient + code, patient + clinical-status, patient + verification-status</td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><code class="highlighter-rouge"><a href="api_clinical_condition.html">Condition </a></code></td>
    <td>patient, patient + clinical-status, patient + category</td>
    <td></td>
    <td></td>
</tr>
<tr>
  <td><code class="highlighter-rouge"><a href="api_management_encounter.html">Encounter</a></code></td>
    <td>patient, patient + date, patient + type, patient + type + date</td>
    <td></td>
    <td></td>
</tr>
<tr>
	<td><code class="highlighter-rouge"><a href="api_medication_immunization.html">Immunization</a></code></td>
    <td>patient, patient + vaccination-procedure-code, patient + notgiven, patient + status</td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><code class="highlighter-rouge"><a href="api_entity_location.html">Location</a></code></td>
    <td>identifier, name, address</td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><code class="highlighter-rouge"><a href="api_medication_medication.html">Medication </a></code></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
  <td><code class="highlighter-rouge"><a href="api_medication_medicationrequest">MedicationRequest</a></code></td>
    <td>patient, patient + status</td>
    <td>MedicationRequest.medication</td>
    <td></td>
</tr>
<tr>
	<td><code class="highlighter-rouge"><a href="api_medication_medicationstatement">MedicationStatement</a></code></td>
    <td>patient, patient + status</td>
    <td>MedicationStatement.medication</td>
    <td></td>
</tr>
<tr>
	<td><code class="highlighter-rouge"><a href="api_diagnostics_observation.html">Observation</a></code></td>
    <td>patient, patient + date, patient + code, patient + date + code</td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><code class="highlighter-rouge"><a href="api_entity_organization.html">Organization</a></code></td>
    <td>identifier, name, address</td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><code class="highlighter-rouge"><a href="api_entity_patient.html">Patient </a></code></td>
    <td>identifier, given, family, birthdate, gender, name, name + gender, name + birthdate, family + gender, given + gender</td>
    <td></td>
    <td></td>
</tr>
<tr>
  <td><code class="highlighter-rouge"><a href="api_entity_practitioner.html">Practitioner</a></code></td>
    <td>identifier, name</td>
    <td></td>
    <td></td>
</tr>
<tr>
	<td><code class="highlighter-rouge"><a href="api_entity_practitioner_role.html">PractitionerRole</a></code></td>
    <td>organization, practitioner</td>
    <td></td>
    <td></td>
</tr>
<tr>
	<td><code class="highlighter-rouge"><a href="api_clinical_procedure.html">Procedure</a></code></td>
    <td>patient, patient + date</td>
    <td></td>
    <td></td>
</tr>


</table>
-->

### 1.3 Capability Statement ###

FHIR Servers MUST support the Care Connect Documents API `Requirements` [Capability Statement](examples/CareConnect-Documents-ServerRequirements-CapabilityStatement-1v0.1.xml){:target="_blank"}

<!--[Demographics Batch Service (DBS)](CareConnect-ServerRequirements-CapabilityStatement-1){:target="_blank"}-->

 

<!--
### 1.4 NHS Number ###

Only verified NHS Number MUST be used with CareConnect profiles. This can be achieved using a spine accredited system, a [Demographics Batch Service (DBS)](https://developer.nhs.uk/library/systems/demographic-batch-service-dbs/){:target="_blank"} batch-traced record (CSV), or using a [Spine Mini Services Provider (HL7v3)](https://nhsconnect.github.io/spine-smsp/){:target="_blank"} to verify the NHS Number.
-->



<!-- include custom/contribute.html content="Get in touch with us to improve the Prerequisites." -->


<!--
## 2. Resource API Structure ##
The FHIR Care Connect profile API's described in the Explore section of this implementation guide have been structured consistently in the following way:
- `0.` References
- `1.` Read
- `2.` Search Parameters
- `3.` Example

### 2.1 Resource API Structure Details ###

<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:20%;">General</th>
<th style="width:80%;">Description </th>
</tr>
<tr>
<td>0. References</td>
<td>Links to other parts of the implementation guide which might help with context and understanding the API's described</td>
</tr>
<tr>
<td>1. Read</td>
<td>A description of how to get the API</td>
</tr>
<tr>
<td>2. Search Parameters</td>
<td>List of search parameters for the profile being described, including any tips for searching. This section shows examples of how to search using the provided search parameters</td>
</tr>
<tr>
<td>3. Example</td>
<td>Description of of the Request & Response headers, example of how to search on a server and the expected response body as an example</td>
</tr>
</table>

## 3. Resource API's ##
This section looks at the Care Connect profile API's covered within this implementation guide.


<table style="min-width:100%;width:100%">
<tr id="clinical">
<th style="width:33%;">Clinical</th>
<th style="width:33%;">&nbsp;</th>
<th style="width:33%;">&nbsp;</th>
</tr>
<tr id="clinicald">
<th>Summary</th>
<th>Diagnostics</th>
<th>Medications</th>
</tr>
<tr>
<td><a href="api_clinical_allergyintolerance.html">AllergyIntolerance</a></td>
<td><a href="api_diagnostics_observation.html">Observation</a></td>
<td><a href="api_medication_medication.html">Medication</a></td>
</tr>
<tr>
<td><a href="api_clinical_condition.html">Condition</a> (Problem)</td>
<td>&nbsp;</td>
<td><a href="api_medication_medicationorder.html">MedicationOrder</a></td>
</tr>
<tr>
<td><a href="api_clinical_procedure.html">Procedure</a></td>
<td>&nbsp;</td>
<td><a href="api_medication_medicationstatement.html">MedicationStatement</a></td>
</tr>
<tr>
<td>&nbsp;</td>
<td>&nbsp;</td>
<td><a href="api_medication_immunization.html">Immunization</a></td>
</tr>
</table>

<table style="min-width:100%;width:100%">
<tr id="base">
<th style="width:33%;">Base</th>
<th style="width:33%;">&nbsp;</th>
<th style="width:33%;">&nbsp;</th>
</tr>
<tr id="based">
<th>Individuals</th>
<th>Entities</th>
<th>Management</th>
</tr>
<tr>
<td><a href="api_entity_patient.html">Patient</a></td>
<td><a href="api_entity_organisation.html">Organization</a></td>
<td><a href="api_management_encounter.html">Encounter</a></td><td></td>
</tr>
<tr>
<td><a href="api_entity_practitioner.html">Practitioner</a></td>
<td><a href="api_entity_location.html">Location</a></td>
<td>&nbsp;</td>
</tr>
<tr>
<td><a href="api_entity_practitioner_role.html">PractitionerRole</a></td>
<td>&nbsp;</td>
<td>&nbsp;</td>
</tr>
</table>


<table style="min-width:100%;width:100%">
<tr id="conformance">
<th style="width:33%;">Foundation</th>
<th style="width:33%;"></th>
<th style="width:33%;"></th>
</tr>
<tr id="conformanced">
<th>Capability</th>
<th></th>
<th>&nbsp;</th>
</tr>
<tr>
<td><a href="api_foundation_capability.html">Capability Statement</a></td>
<td></td>
<td>&nbsp;</td>
</tr>
<tr>
<td></td>
<td></td>
<td>&nbsp;</td>
</tr>
</table>
-->