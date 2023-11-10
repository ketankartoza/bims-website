---
title: BIMS Documentation
summary: Central documentation site for BIMS projects
    - Tim Sutton
    - Helen Dallas
    - Jeremy Prior
date: 26-09-2023
some_url: https://github.com/kartoza/bims-website
copyright: Copyright 2023, Kartoza
contact: 
license: This program is free software; you can redistribute it and/or modify it under the terms of the GNU Affero General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.
#context_id: 1234
---

# Filtering

Two types of filters are supported on FBIS: Contextual filters, which filter based on the site or collection record attributes in the database, and map based filters which operate by selection of sites on the map.

## Contextual filters

One of the key technologies ‘under the hood’ in FBIS is the use of Kartoza’s GeoContext service. GeoContext provides a way to, in a single query, obtain contextual data for any geographical point across multiple Open Geospatial Consortium (OGC) web services (WMS, WFS). The results are aggregated into a single document and made available to FBIS which then stores this aggregate data as properties of a site. Having this rich collection of GeoContext data for each site allows us to filter the records shown on the map and in dashboards in fairly arbitrary ways. For example, selecting only records from a given catchment or ecoregion. A description of each filter is provided in Table 1.  

Filtering is done using a hierarchical ‘tree view’ in the filter panel (Figure 4). Tree nodes can be expanded or collapsed and selecting a specific node or set of nodes will allow you to apply the selected filters to the records displayed on the map and search result areas as shown below:

**Example of some of the filters available for querying the data.**

![Contextual Filter 1](img/contextual-filter-1.png)

To apply the filter click **Apply**; to clear the click **Clear**.

![Contextual Filter 2](img/contextual-filter-2.png)

### Table 1. Details of the filters provided in FBIS

<!-- The <br>'s in the 'spatial' and 'Origin and endemism' cells are to allow for the lists -->
| Filter | Description |
| -- | -- |
| ![Contextual Filter 3](img/contextual-filter-3.png) | **Biodiversity module:** Filter records for fish, invertebrates, algae, adult odonates or anuran only by clicking the appropriate icon. To filter records for sites that have more than one biodiversity module (e.g. fish and invertebrates), use the Shift Click function to select multiple modules. |
| ![Contextual Filter 4](img/contextual-filter-4.png) | **Abiotic module:** Filter records for sites that have water temperature time series data, or physico-chemical data. |
| ![Contextual Filter 5](img/contextual-filter-5.png) | **Data sources:** The default setting in FBIS is all data collated specifically for FBIS, existing GBIF records and existing Virtual Museum records are provided. Uncheck those sources that you do not want records for. Note that neither GBIF or Virtual Museum data have not been validated by the FBIS team. |
| ![Contextual Filter 6](img/contextual-filter-6.png) | **Validation status:** The default setting in FBIS is that all Validated, unvalidated, SASS Accredited and Non SASS Accredited data are provided. Validated data have been checked by FBIS admin and /or designated expert, while unvalidated data have not been checked. SASS Accredited and Non SASS Accredited relates specifically to whether the assessor was SASS accredited at the time of doing the SASS assessment. Filter records by checking the relevant boxes to include specific data only. |
| ![Contextual Filter 7](img/contextual-filter-7.png) | **Temporal:** Filter records using the sliding scale to specify year(s), and/or check specific months. |
| ![Contextual Filter 8](img/contextual-filter-8.png) | **Spatial:** Thirteen spatial filters are currently provided for users to filter the records shown on the map and in dashboards. For example, selecting only records from a given province, catchment or SA ecoregion. Further details are provided in [section 7.2](mapping.md). The current list of spatial filters lodged in FBIS include:<br> - Geomorphological Zones<br> - Freshwater Ecoregions of the World<br> - South African Province and Neighbouring Country<br> - Management Area<br> - Catchments<br> - SA Ecoregions<br> - National and Provincial Critical Biodiversity Areas<br> - National Freshwater Ecosystem Priority Areas<br> - Strategic Water Source Areas<br> - National Biodiversity Assessments 2018<br> - Hydrological Regions<br> - Thermal Framework |
| ![Contextual Filter 9](img/contextual-filter-9.png) | **Ecological category (SASS):** Filter records based on ecological categories, interpreted from SASS data interpretation guidelines of Dallas (2007). |
| ![Contextual Filter 10](img/contextual-filter-10.png) | **Origin and endemism:** Filter records based on origin: native or non-native, where non-native includes both alien and extralimital taxa. Filter records based on endemism, where taxa are divided into eight categories as follows:<br> - Micro-endemic level 2 (Endemic to a single river or wetland)<br> - Micro-endemic level 1 (Endemic to less than 5 rivers or wetlands)<br> - Regional endemic level 2 (Endemic to a single primary catchment)<br> - Regional endemic level 1 (Endemic to a single Freshwater Ecoregion (e.g. CFE), more than one primary catchment)<br> - National endemic (Endemic to South Africa, occurs in more than one Freshwater Ecoregion within SA)<br> - Subregional endemic (Endemic to southern Africa)<br> - Widespread (Occurs beyond southern Africa)<br> - Unknow (Endemism is unknown) |
| ![Contextual Filter 11](img/contextual-filter-11.png) | **Conservation status:** Derived from the International Union for Conservation of Nature’s (IUCN) Red List of Threatened Species, a user may filter records based on global conservation status. |
| ![Contextual Filter 12](img/contextual-filter-12.png) | **Reference category:** Filter records based on type of reference. |
| ![Contextual Filter 13](img/contextual-filter-13.png) | **Study reference:** Filter records by selecting a specific study reference. |
| ![Contextual Filter 14](img/contextual-filter-14.png) | **Owner:** Filter records collected by a specific person. |
| ![Contextual Filter 15](img/contextual-filter-15.png) | **Decision support tool:** Filter records that have been used to support management and conservation decision making by contributing to a specific Decision Support Tool. |

Applying a filter returns a subset of the data based on your filter criteria, for example records in SA Ecoregion = Western Folded Mountains.  When a filter is in effect, you will see a yellow highlight of the ‘drawers’ which have filter options enabled (highlighted in yellow). The filter system only displays filter options for categories that have sites associated. For example, if you do not see an option in the ‘Provinces’ filter for Northern Cape, it means we do not have any data (sites) for that province.

**Filtering sites to show only those in SA Ecoregion = Western Folded Mountains:**

![Contextual Filter 16](img/contextual-filter-16.png)

**Highlighting drawers where a filter condition is active:**

![Contextual FIlter 17](img/contextual-filter-17.png)

## Map based filtering

Sites may also be selected by using Lasso Control. This feature allows the user to draw a polygon around specific sites to include in dashboards. By clicking “Update search” the user will see the search results for all the sites in the polygon. Note that to close your lasso selection you must click on the starting point again.  The “Merge sites” feature allows the administrator to merge the data from the sites in the polygon into one site. The clear Polygon, resets to zero.

**Drawing a polygon to select and group sites:**

![Map Based Filter 1](img/map-based-filter-1.png)
