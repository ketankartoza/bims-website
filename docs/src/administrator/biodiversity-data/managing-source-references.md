---
title: BIMS Documentation
summary: Central documentation site for BIMS projects
    - Tim Sutton
    - Helen Dallas
    - Jeremy Shelton
    - Jeremy Prior
date: 01-08-2022
some_url: https://github.com/kartoza/bims-website
copyright: Copyright 2023, Kartoza
contact: 
license: This program is free software; you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.
#context_id: 1234
---

# Managing Source references

A specific administration module has been developed to allow administrators to manage metadata and citations associated with each biological occurrence record.

![Managing Source References 1](./img/managing-source-references-1.png)

Only registered users with super user status are able to access **Source References**, typically the administrators.

All biodiversity data served need to have associated Metadata, which is visible in the metadata table in the dashboards. This metadata allows the users to establish exactly where the data originated from and to navigate to the study reference if desired.

![Managing Source References 2](./img/managing-source-references-2.png)

## Types of source references

Multiple sources of taxon occurrence data generally exist, although this is highly dependent on the country. Potential sources of biodiversity data include the following source reference categories:

* Peer-reviewed scientific articles
* Theses
* Published reports
* Databases
* Unpublished data

The following sections provide details of the recommended processes for sourcing taxon occurrence data from the different reference categories. This is done by all users adding data and by administrators.

### Peer-reviewed scientific article

Data from peer-reviewed scientific articles are best sourced by undertaking a literature search using Google Scholar. To ensure that relevant papers are identified, appropriate search term combination should be used. For example, for all native freshwater fishes in South Africa: “Genus species” & “South Africa” (where “Genus species” represents the scientific name for each taxon).  It is important that search terms are clearly-defined and consistent, so that the process is repeatable and defensible.

### Thesis

University theses are easily searched using relevant university search engines. Often local experts also know of relevant theses and can be contacted directly. Where possible, electronic data should be sourced directly from individuals, as this saves significant time that would otherwise be occupied in transcription of paper to digital records during data consolidation.

### Published report

Technical and consultancy reports are often difficult to source and requires knowledge of local experts who have undertaken relevant studies. Where possible, electronic data should be sourced directly from individuals, as this saves significant time during data consolidation.

### Database

Identify and contact relevant organisations who may have data to share that is already in a database. Data sharing agreements may be needed depending on the organisation. For organisation that regularly add data it is useful to set up a database in the organisation’s name.

### Unpublished data

Identify individuals who may have data to share. Where possible, electronic data should be sourced directly from individuals, as this saves significant time during data consolidation.

Source reference system can store either an electronic document (e.g. by attaching a PDF to the document record) or a link to an online resource (URL). The order of preference should be:

1. Use DOI based citations wherever possible (in which case the URL attribute described below should not be needed).
2. Use documents with references to external resources (i.e. a URL that points to a published PDF on a web site).
3. Used documents with attached PDF as a last resort (this will require first uploading the document in the document management system and then providing the link to the uploaded document  in the metadata table described below).

## Adding source references to occurrence data

Source references are either added when data are added using the data capture forms on FBIS, or when uploading occurrence data using the data upload excel file. (See **Preparing and checking an Occurrence Data File before uploading**).

### Adding a source reference using data capture forms

When adding data, three data capture forms are shown in sequence, namely 1) an occurrence record form, where you capture which taxa were present; 2) an abiotic data form where you capture physico-chemical and other abiotic data; and 3) a source reference for records form, where you capture the source reference or metadata for the biological record.

![Managing Source References 3](./img/managing-source-references-3.png)

### Peer-reviewed scientific articles

Select the reference category and insert the DOI or URL and click the search button. The citation is then retrieved via an online citation management system and inserted. Click Submit to save.

![Managing Source References 4](./img/managing-source-references-4.png)

### Published reports and theses

Select the reference category and select from the dropdown list of titles, if the published report or thesis is already uploaded, or select “Upload new” to add a new published report or thesis.

![Managing Source References 5](./img/managing-source-references-5.png)

When uploading a new published report or thesis, complete the fields using the format indicated including Author(s), Year, Source, Title, Description (if desired) and Url or upload file. Confirm that you are owner of the document being added and Upload. This is then submitted.

![Managing Source References 6](./img/managing-source-references-6.png)

![Managing Source References 7](./img/managing-source-references-7.png)

### Databases

Select the reference category and select from the dropdown list of databases, if the database is already created, or select “Add new” to add a new database.

![Managing Source References 8](./img/managing-source-references-8.png)

When adding a new database, complete the name and provide a description. Add the url if it exists and click create. Add notes if desired.

![Managing Source References 9](./img/managing-source-references-9.png)

### Unpublished data

Select the reference category and select from the dropdown list under notes. If the unpublished dataset exists, select the unpublished dataset name, or if the unpublished dataset needs to be created, select “Add new” to add a new unpublished dataset. In the notes, add the name of the person, details of the study and date if possible or applicable.

![Managing Source References 10](./img/managing-source-references-10.png)

## Adding a source reference using occurrence upload excel files

Where data are uploaded using the Data Upload Templates, the data capturer needs to specify the following:

* **Author(s)**: Surname + Initials
* **Year**: Year of study
* **Source**: Details such as journal name, report, thesis, database and unpublished data.
* **Title**: Title of the report. thesis, database or unpublished dataset.
* **Reference category**: Select from dropdown options
* **URL**: Thesis handle, or article link if no DOI available
* **DOI**: DOI for reference ( e.g. 10.2989/16085914.2018.1491385) – the citation for articles with DOIs is done automatically.
* **Document Upload Link**: Link to "Source Reference" page after uploading PDF or URL of published report or thesis.

When adding occurrence data using the upload excel files, the following columns are populated for each reference category:

### Using Source References as an administrator

Errors can arise when source references are added to the information system by users. These can be picked up and fixed by undertaking various filters, checking and edits, including those listed below.

* Search for a reference type or category
        ![Managing Source References 11](./img/managing-source-references-11.png)
* Search by author(s)
        ![Managing Source References 12](./img/managing-source-references-12.png)
* Search using free text
        ![Managing Source References 13](./img/managing-source-references-13.png)

Once the source reference has been found, it can be updated, deleted (only if there are not records associated with it), and the Document ID can be copied. This is needed when uploading occurrence records using the excel template.

![Managing Source References 14](./img/managing-source-references-14.png)

By clicking on the records button you can check exactly which sites and data are linked to the source reference.
