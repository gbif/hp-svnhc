---
layout: documentation
permalink: /en/data-aggregator-faqs
title: Data Aggregator
toc: true
sideNavigation: sideNavigation.tutorials
---

# Swiss Data Aggregator


# FAQs

## Do I have to upload my entire database into the Data Aggregator?

There is no need to upload all of your database into the Data Aggregator. You can choose to upload only the most important fields for a selected set of records. The key element in the aggregator is the [catalogNumber field](https://svnhc.hp.gbif-staging.org/en/data-aggregator#minimal-mandatory-fields-of-the-data-aggregator), which has to be unique for all of your records. If a given **catalogNumber value does not yet exist** in your Data Aggregator Collection, then it is **created when importing** a dataset. If a given **catalogNumber value already exists** on the Data Aggregator Collection, then its attributes (other fields) are simply **updated** when importing a dataset.

To help you select your fields, **here is a table with the most important Darwin Core terms** and an example line. You can use it to organise your dataset for the upload into the Data Aggregator.

<div style="overflow-x: auto;">
  <table style="background-color: {{ site.data.colors.lightgreen.transparency }}; width: 100%; border-collapse: collapse; border: 1px solid black;">
    <tr>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">scientificName</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">acceptedNameUsage</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">family</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">basisOfRecord</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">partOfOrganism</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">catalogNumber</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">recordedBy</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">recordedByID</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">recordNumber</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">eventDate</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">continent</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">higherGeography</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">country</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">countryCode</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">stateProvince</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">locality</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">decimalLatitude</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">decimalLongitude</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">geodeticDatum</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">coordinateUncertaintyInMeters</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">verbatimElevation</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">identifiedBy</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">identifiedByID</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">rightsHolder</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">institutionCode</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">institutionID</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">collectionCode</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">collectionID</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">preparations</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">typeStatus</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">yearCollectionEntrance</th>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px; text-align: left;"><i>Pinus picea</i> L.</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;"><i>Abies alba</i> Mill.</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Pinaceae</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">PreservedSpecimen</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">plant tissue</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">inventory-1234</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Weber Morgan</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">0000-0002-1043-7587</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">MW-54</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">2015-06-28</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Europe</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Alpen</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Switzerland</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">CH</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Bern</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Luuswald, above Iseltwald</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">46.701815</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">7.971722</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">WGS84</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">500</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">1050-1120 m</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Weber Morgan</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">0009-0000-0012-XXXX</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">(c) Herbarium X</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">X</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">g9pdh657-3268-4d51-j015-314k3528y74y</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">General collection</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">t62v83k3-3zs9-6934-kk21-o49ra9e7348p</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">dried plant</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">Not a type</td>
      <td style="border: 1px solid black; padding: 5px; text-align: left;">2015</td>
    </tr>
  </table>
</div>

<br><br>
The Darwin Core Github repository also offers files with all or a selection of the Darwin Core fields : [Github tdwg/dwc/dist](https://github.com/tdwg/dwc/tree/master/dist){:target="_blank"}

## What is Darwin Core?

[Darwin Core](https://dwc.tdwg.org/){:target="_blank"} is a **data standard**, a template to be used when organising data in a database or a table in order to have **distinct and precise fields with a known and fixed information format** in each of them. It has been created as a helping basis to make [FAIR](https://dwc.tdwg.org/ ){:target="_blank"} data.

The direct benefit of the Darwin Core standard is the **high level of compatibility between data from different sources**.

### How is Darwin Core organised?

Each **term** of Darwin Core has a **precise and unique definition**, and for some a **controlled vocabulary** is highly recommended. The **terms** are organised in **categories**, based on the data they must contain. Concerning data of natural history institutions, the categories could correspond to these following themes:

<table border="1">
  <tr>
    <th>Theme</th>
    <th>Categories in Darwin Core</th>
  </tr>
  <tr>
    <td><strong>⛰️ Field work</strong></td>
    <td>
      <table>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#occurrence" target="_blank">Occurrence</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#measurementorfact" target="_blank">MeasurementOrFact</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#organism" target="_blank">Organism</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#livingspecimen" target="_blank">LivingSpecimen</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#materialsample" target="_blank">MaterialSample</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#humanobservation" target="_blank">HumanObservation</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#event" target="_blank">Event</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#machineobservation" target="_blank">MachineObservation</a></td>
        </tr>
      </table>
    </td>
  </tr>
  <tr>
    <td><strong>🗄️ Specimen storage</strong></td>
    <td>
      <table>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#organism" target="_blank">Organism</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#preservedspecimen" target="_blank">PreservedSpecimen</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#materialentity" target="_blank">MaterialEntity</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#fossilspecimen" target="_blank">FossilSpecimen</a></td>
        </tr>
        <tr>
         <td><a href="https://dwc.tdwg.org/terms/#materialsample" target="_blank">MaterialSample</a></td>
        </tr>
      </table>
    </td>
  </tr>
  <tr>
    <td><strong>🖥️ Database management</strong></td>
    <td>
      <table>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#record-level" target="_blank">Record-level</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#measurementorfact" target="_blank">MeasurementOrFact</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#occurrence" target="_blank">Occurrence</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#resourcerelationship" target="_blank">ResourceRelationship</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#organism" target="_blank">Organism</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#livingspecimen" target="_blank">LivingSpecimen</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#event" target="_blank">Event</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#materialcitation" target="_blank">MaterialCitation</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#identification" target="_blank">Identification</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#humanobservation" target="_blank">HumanObservation</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#taxon" target="_blank">Taxon</a></td>
        </tr>
      </table>
    </td>
  </tr>
  <tr>
    <td><strong>🐟 Taxonomy</strong></td>
    <td>
      <table>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#identification" target="_blank">Identification</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#taxon" target="_blank">Taxon</a></td>
        </tr>
      </table>
    </td>    
  </tr>
  <tr>
    <td><strong>🌍 Geography</strong></td>
    <td>
      <table>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#occurrence" target="_blank">Occurrence</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#geologicalcontext" target="_blank">GeologicalContext</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#event" target="_blank">Event</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#taxon" target="_blank">Taxon</a></td>
        </tr>
        <tr>
          <td><a href="https://dwc.tdwg.org/terms/#location" target="_blank">Location</a></td>
          <td><a href="https://dwc.tdwg.org/terms/#measurementorfact" target="_blank">MeasurementOrFact</a></td>
        </tr>
      </table>
    </td>
  </tr>
</table>

### Where can I find the Darwin Core terms description?
On the Darwin Core official website, the [Quick Reference Guide](https://dwc.tdwg.org/terms/) is the easiest to use.

Here are a few of the top-10 most used fields in natural history institutions' databases. The ones marked with a "!" should use only a [controlled vocabulary](https://svnhc.hp.gbif-staging.org/en/data-aggregator/#what-is-a-controlled-vocabulary).

| DwC term (dwc:) | DwC Definition | Corresponding terms found in NHC datasets | Examples |
| --------------- | -------------- | ----------------------------------------- | -------- |
| ! [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName){:target="_blank"} | **class [Taxon](https://dwc.tdwg.org/terms/#taxon){:target="_blank"}** <br> The **full scientific name**, with authorship and date information if known, **or** the name in **lowest level taxonomic rank that can be determined**. | Scientific name<br> nom scientifique<br> Wissenschaftliche Name<br> Full name<br> Nom complet | _Cyclamen hederifolium_ Aiton<br> _Vulpes vulpes (Linnaeus, 1758)_ |
| ! [eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target="_blank"} | **class [Event](https://dwc.tdwg.org/terms/#event){:target="_blank"}**<br> The date-time or interval when the dwc:Event was recorded. Format: for a precise date: YYYY-MM-DD, for an interval: YYYY-MM-DD/YYYY-MM-DD | date of collect<br>  collection date<br>  date de récolte<br>  Funddatum | 1903-08<br> 2024-08-01<br> 1815 |
| ! [recordedBy](https://dwc.tdwg.org/terms/#dwc:recordedBy){:target="_blank"} | **class [Occurrence](https://dwc.tdwg.org/terms/#occurrence){:target="_blank"}**<br> A list (concatenated and separated) of names of people, groups, or organizations responsible for recording the original dwc:Occurrence. | Collector<br> collecteur<br> leg. | Sutter Ruben<br> Steffen Liseli<br> Dutoit Eugen |
| [recordNumber](https://dwc.tdwg.org/terms/#dwc:recordNumber){:target="_blank"} | **class [Occurrence](https://dwc.tdwg.org/terms/#occurrence){:target="_blank"}**<br> An identifier given to the dwc:Occurrence at the time it was recorded (link between field notes and specimen). | field number<br> collect number<br> numéro de récolte<br> Fundnummer | 2089<br> ASM-515 |
| [catalogNumber](https://dwc.tdwg.org/terms/#dwc:catalogNumber){:target="_blank"} | **class [Occurrence](https://dwc.tdwg.org/terms/#occurrence){:target="_blank"}**<br> A unique identifier for the record within the data set or collection. | Code-barre<br> Numéro<br> Barcode<br> Nummer<br> Numéro d'inventaire | G00009201<br> Sheet-2765149 |
| ! [country](https://dwc.tdwg.org/terms/#dwc:country){:target="_blank"} | **class [Location](https://dwc.tdwg.org/terms/#location){:target="_blank"}**<br> The name of the country or major administrative unit in which the [dcterms:Location](https://dwc.tdwg.org/terms/#location) occurs. | Pays<br> Land<br> Country | Switzerland<br> France<br> Germany<br> Italy<br> Austria |
| [verbatimLocality](https://dwc.tdwg.org/terms/#dwc:verbatimLocality){:target="_blank"} | **class [Location](https://dwc.tdwg.org/terms/#location){:target="_blank"}**<br> The original textual description of the place. | Location<br> Fundort<br> Lieu | "Les Follatères"<br> "Zürich, am See"<br> "Pizzo Leone, 1659 m" |
| ! [locality](https://dwc.tdwg.org/terms/#dwc:locality){:target="_blank"} | **class [Location](https://dwc.tdwg.org/terms/#location){:target="_blank"}**<br> The specific description of the place. | _often not standardised in databases_ | "Les Follatères"<br> "Lake of Zürich"<br> "Pizzo Leone, summit" |
| ! [institutionCode](https://dwc.tdwg.org/terms/#dwc:institutionCode){:target="_blank"} | **class [Record-level](https://dwc.tdwg.org/terms/#record-level){:target="_blank"}**<br> The name (or acronym) in use by the institution having custody of the object(s) or information referred to in the record. | Institution | G<br> UZH:Z<br> BERN |
| ! [collectionCode](https://dwc.tdwg.org/terms/#dwc:collectionCode){:target="_blank"} | **class [Record-level](https://dwc.tdwg.org/terms/#record-level){:target="_blank"}**<br> The name, acronym, coden, or initialism identifying the collection or data set from which the record was derived. | Collection | General collection<br> Collection générale<br> Hauptsammlung |

### What is a controlled vocabulary?

A controlled vocabulary is a **standardized set of terms and phrases used to ensure consistency and accuracy in the documentation and cataloging of specimens**. This vocabulary facilitates **clear communication**, **data sharing**, and **interoperability** among researchers, institutions, and databases by providing a **common language** for describing attributes such as species, locations, and collection methods. Darwin Core is widely used for biodiversity data, to ensure that everyone uses the same terms in the same way when recording and sharing information about natural history collections.

| Existing name for a field (and DwC term) | Without controlled vocabulary | With controlled vocabulary | Reference system |
| ---------------------------------------- | ----------------------------- | -------------------------- | ---------------- |
| Name<br> Art<br> Espèce<br><br> [dwc:scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName){:target="_blank"} | Cyclamen hederifolium<br> C. hederifolium<br> C. hed.<br> Cyclamen hederifolium Aiton<br> hederifolium | *Cyclamen hederifolium* Aiton | [World Flora Online](https://www.worldfloraonline.org/){:target="_blank"}<br> [GBIF.org](https://www.gbif.org/){:target="_blank"}<br> [Catalog of Life](https://www.catalogueoflife.org/){:target="_blank"}<br> [Info Species, Swiss centers of information](https://www.infospecies.ch/de/){:target="_blank"} |
| Date of collect<br> Funddatum<br> Date de récolte<br><br> [dwc:eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target="_blank"} | 1. August 2024<br> 1er août 2024<br> 1° agosto 2024<br> 1 Aug. 2024<br> 1.8.2024<br> 01 VIII 2024<br> 1/8/24<br> 8/1/2024  | 2024-08-01 | [ISO 8601-1:2019](https://www.iso.org/obp/ui/en/#iso:std:iso:8601:-1:ed-1:v1:en){:target="_blank"} |
| leg.<br><br> [dwc:recordedBy](https://dwc.tdwg.org/terms/#dwc:recordedBy){:target="_blank"} | Ruben Sutter<br> R. Sutter<br> Sutter<br> RSutter<br> R.S. | Sutter Ruben<br> + Q96409968 ([recordedByID](https://dwc.tdwg.org/terms/#dwc:recordedByID){:target="_blank"})  | [ORCID](https://orcid.org/){:target="_blank"} (alive scientists)<br> [WIKIDATA](https://www.wikidata.org/wiki/Wikidata:Main_Page){:target="_blank"} (older scientists) |
| Country<br> Pays<br> Land<br><br> [dwc:country](https://dwc.tdwg.org/terms/#dwc:country){:target="_blank"} | Schweiz<br> Suisse<br> Switzerland<br> Svizzera<br> Svizra<br> CH | Switzerland | [Getty Thesaurus of Geographic Names](https://www.getty.edu/research/tools/vocabularies/tgn/){:target="_blank"} |
| Locality<br><br> [dwc:locality](https://dwc.tdwg.org/terms/#dwc:locality){:target="_blank"} | Les Follatères<br> N of Sion, on the right side of the Rhône river, lieu-dit Les Follatères<br> Follatères | Les Follatères | [Getty Thesaurus of Geographic Names](https://www.getty.edu/research/tools/vocabularies/tgn/){:target="_blank"}<br> [swissNAMES3D](https://www.swisstopo.admin.ch/en/landscape-model-swissnames3d){:target="_blank"} |
| Institution<br><br> [dwc:institutionCode](https://dwc.tdwg.org/terms/#dwc:institutionCode){:target="_blank"} | Herbarium des Botanischen Gartens der Universität Bern<br> Herbarium Bern<br> Herb. Bern<br> Herbarium BOGA | BERN | [GRSciColl](https://scientific-collections.gbif.org/){:target="_blank"} |
| collection<br><br> [dwc:country](https://dwc.tdwg.org/terms/#dwc:country){:target="_blank"} | Hauptsammlung | Herbarium specimens | [GRSciColl](https://scientific-collections.gbif.org/){:target="_blank"} |


## But my database/dataset is not formatted in Darwin Core, do I have to change everything?

Rest assured, you do not need to change your database/dataset dramatically. The most important thing is to find the easiest and fastest way to adapt your database/dataset to import it in the data aggregator. Here are our 3 most popular suggestions:


<div style="display: flex; justify-content: space-between; align-items: flex-start;">
  <div style="flex: 3; padding-right: 70px;"><strong>1) Add the <a href="https://dwc.tdwg.org/terms/">Darwin Core terms</a></strong> in your dataset/database as new columns. With the help of <strong>scripts</strong> and <strong>formulas</strong>, pick the fields of your database and copy or adapt their values in the DwC fields in a dynamic way.
  <br><br>
  <table style="background-color: {{ site.data.colors.lightpink.transparency }}; width: 100%; border-collapse: collapse; border: 1px solid black;">
  <tr>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightpink.background }};">Barcode</th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightpink.background }};"><a href="https://dwc.tdwg.org/terms/#dwc:catalogNumber" target="_blank">catalogNumber</a></th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightpink.background }};">Species</th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightpink.background }};"><a href="https://dwc.tdwg.org/terms/#dwc:scientificName" target="_blank">scientificName</a></th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightpink.background }};">...</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 5px;">XXX-0123456</td>
    <td style="border: 1px solid black; padding: 5px;">XXX-0123456</td>
    <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i></td>
    <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i> Aiton</td>
    <td style="border: 1px solid black; padding: 5px;">...</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 5px;">XXX-7891011</td>
    <td style="border: 1px solid black; padding: 5px;">XXX-7891011</td>
    <td style="border: 1px solid black; padding: 5px;"><i>C. hederifolium</i></td>
    <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i> Aiton</td>
    <td style="border: 1px solid black; padding: 5px;">...</td>
  </tr>
  </table>
  </div>
  
  <div style="flex: 1;">
    ✅ Darwin Core named columns/fields<br>
    ✅ No changes of original columns/fields<br>
    ❌ Duplicated in multiple columns<br>
    ❌ If not dynamic, then mistakes can lower the dataset/database quality
  </div>
</div>
<br><br>

<div style="display: flex; justify-content: space-between; align-items: flex-start;">
  <div style="flex: 3; padding-right: 70px;"><strong>2) Replace the name of your fields with the corresponding <a href="https://dwc.tdwg.org/terms/">Darwin Core term</a></strong> after checking your field compatibilities with the DwC terms definitions.
  <br><br>
  <table style="background-color: {{ site.data.colors.lightblue.transparency }}; width: 100%; border-collapse: collapse; border: 1px solid black;">
  <tr>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightblue.background }};"><s>Barcode</s><br><a href="https://dwc.tdwg.org/terms/#dwc:catalogNumber" target="_blank">catalogNumber</a></th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightblue.background }};"><s>Species</s><br><a href="https://dwc.tdwg.org/terms/#dwc:scientificName" target="_blank">scientificName</a></th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightblue.background }};">...</th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightblue.background }};"><s>Date of collect</s><br><a href="https://dwc.tdwg.org/terms/#dwc:eventDate" target="_blank">eventDate</a></th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 5px;">XXX-0123456</td>
    <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i> Aiton</td>
    <td style="border: 1px solid black; padding: 5px;">...</td>
    <td style="border: 1px solid black; padding: 5px;"><s>12 VIII 1905</s><br>1905-08-12</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 5px;">XXX-7891011</td>
    <td style="border: 1px solid black; padding: 5px;"><s><i>C. hederifolium</i></s><br><i>Cyclamen hederifolium</i> Aiton</td>
    <td style="border: 1px solid black; padding: 5px;">...</td>
    <td style="border: 1px solid black; padding: 5px;">1968-06-12</td>
  </tr>
  </table>
  </div>
  
  <div style="flex: 1;">
    ✅ Fully Darwin Core compatible dataset/database<br>
    ✅ No more changes in the future<br>
    ❌ Difficult to change habits regarding field names<br>
    ❌ Needs a deep cleaning of the whole database/dataset
  </div>
</div>
<br><br>

<div style="display: flex; justify-content: space-between; align-items: flex-start;">
  <div style="flex: 3; padding-right: 70px;"><strong>3) Export a selected set of your database fields and make the correspondance with the <a href="https://dwc.tdwg.org/terms/">Darwin Core terms</a></strong>. Adapt your data with the other important DwC terms until all of the information you want to export is ready.
  <br><br>
  <p style="text-align: center; font-size: 18px;"><u>Your original data</u></p>
  <table style="background-color: {{ site.data.colors.lightgreen.transparency }}; width: 100%; border-collapse: collapse; border: 1px solid black;">
    <tr>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">Barcode</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">Species</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">Date of collect</th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">Storage room</th>
     <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};">...</th>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">XXX-0123456</td>
      <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i></td>
      <td style="border: 1px solid black; padding: 5px;">12 VIII 1905</td>
      <td style="border: 1px solid black; padding: 5px;">General collection</td>
      <td style="border: 1px solid black; padding: 5px;">...</td>
    </tr>
    <tr>
     <td style="border: 1px solid black; padding: 5px;">XXX-7891011</td>
     <td style="border: 1px solid black; padding: 5px;"><i>C. hederifolium</i></td>
     <td style="border: 1px solid black; padding: 5px;">23.6.68</td>
     <td style="border: 1px solid black; padding: 5px;">Regional collection</td>
     <td style="border: 1px solid black; padding: 5px;">...</td>
    </tr>
  </table>
  
  <p style="text-align: center; font-size: 50px;">+</p>
  <p style="text-align: center; font-size: 18px;"><u>Table imported in the Aggregator</u></p>
  
  <table style="background-color: {{ site.data.colors.lightgreen.transparency }}; width: 100%; border-collapse: collapse; border: 1px solid black;">
    <tr>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};"><a href="https://dwc.tdwg.org/terms/#dwc:catalogNumber" target="_blank">catalogNumber</a></th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};"><a href="https://dwc.tdwg.org/terms/#dwc:scientificName" target="_blank">scientificName</a></th>
      <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: {{ site.data.colors.lightgreen.background }};"><a href="https://dwc.tdwg.org/terms/#dwc:eventDate" target="_blank">eventDate</a></th>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">XXX-0123456</td>
      <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i> Aiton</td>
      <td style="border: 1px solid black; padding: 5px;">1905-08-12</td>
    </tr>
    <tr>
      <td style="border: 1px solid black; padding: 5px;">XXX-7891011</td>
      <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i> Aiton</td>
      <td style="border: 1px solid black; padding: 5px;">1968-06-23</td>
    </tr>
  </table>
  </div>
  
  <div style="flex: 1;">
    ✅ No extra work of restructuring your database<br>
    ✅ Full control of the data you share<br>
    ❌ Duplicated data<br>
    ❌ Extensive preparation work for every update of the data online
  </div>

</div>
<br><br>

## Which fields are required/mandatory?

### Minimal mandatory fields of the Data Aggregator

| DwC term | DwC definition | In most databases | Examples |
| -------- | -------------- | ----------------- | -------- |
| [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName){:target="_blank"} | The full scientific name, with authorship and date information if known, or the name in lowest level taxonomic rank that can be determined. | Scientific name<br> nom scientifique<br> Wissenschaftliche Name<br> Full name<br> Nom complet | _Cyclamen hederifolium_ Aiton<br> _Vulpes vulpes_ (Linnaeus, 1758) |
| [catalogNumber](https://dwc.tdwg.org/terms/#dwc:catalogNumber){:target="_blank"} | A unique identifier for the record within the data set or collection. | Code-barre<br> Numéro<br> Barcode<br> Nummer<br> Numéro d’inventaire | G00009201<br> Sheet-2765149

### Additional fields increasing data quality in the Data Aggregator (MIDS)
The [MIDS](https://www.tdwg.org/community/cd/mids/){:target="_blank"} is the **M**inimum **I**nformation about a **D**igital **S**pecimen. The four levels of MIDS (0, 1, 2, 3) expected in the Data Aggregator correspond to the minimal expected information to be present when publishing on GBIF. All of the expected fields have to be present and contain data for a record to reach the corresponding MIDS quality level.

| MIDS | DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| ---- | --------------- | ---------- | ------------------------------------- | -------- |
| 0 | [institutionCode](https://dwc.tdwg.org/terms/#dwc:institutionCode){:target='_blank'} | The name (or acronym) in use by the institution having custody of the object(s) or information referred to in the record. <br> See the [GrSciColl official institution codes](https://scientific-collections.gbif.org/institution/search?country=CH){:target="_blank"} | ... | BERN<br> G<br> MHNN |

| MIDS | DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| ---- | --------------- | ---------- | ------------------------------------- | -------- |
| 1 | _part_of_organism_ ! _not DwC_ ! | Part or parts of the organism that have been preserved. | ... | shell<br> skeleton<br> skull<br> soft tissue |
| 1 | [preparations](https://dwc.tdwg.org/terms/#dwc:preparations){:target='_blank'} | A list (concatenated and separated) of preparations and preservation methods for a specimen. | ... | fossil<br> cast<br> photograph<br> DNA extract<br> skin<br> skull<br> skeleton<br> whole animal (ETOH)<br> tissue (EDTA) |


| MIDS | DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| ---- | --------------- | ---------- | ------------------------------------- | -------- |
| 2 | _yearCollectionEntrance_ ! _not DwC_ ! | The four-digit year of collection entrance of a specimen (earliest year of occurrence in absence of a documented collection event). | ... | ... |
| 2 | [collectionCode](https://dwc.tdwg.org/terms/#dwc:collectionCode){:target='_blank'} | The name, acronym, coden, or initialism identifying the collection or data set from which the record was derived. | ... | ... |
| 2 | [collectionID](https://dwc.tdwg.org/terms/#dwc:collectionID){:target='_blank'} | An identifier for the collection or dataset from which the record was derived. | ...    | ... |
| 2 | [eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target='_blank'} | The date-time or interval during which a dwc:Event occurred. For occurrences, this is the date-time when the dwc:Event was recorded. Not suitable for a time in a geological context. | date of collect<br> collection date<br> date de récolte<br> Funddatum<br> date<br> Datum | August 1903<br> 01.04.85<br> 15 VII 1867 |
| 2 | [recordedBy](https://dwc.tdwg.org/terms/#dwc:recordedBy){:target='_blank'} | A list (concatenated and separated) of names of people, groups, or organizations responsible for recording the original Occurrence. The primary collector or observer, especially one who applies a personal identifier (recordNumber), should be listed first. | leg.<br> collecteur<br> Sammler<br> collector  | ... |
| 2 | [typeStatus](https://dwc.tdwg.org/terms/#dwc:typeStatus){:target='_blank'} | A list (concatenated and separated) of nomenclatural types (type status, typified scientific name, publication) applied to the subject. | type | ... |
| 2 | [continent](https://dwc.tdwg.org/terms/#dwc:continent){:target='_blank'} | The name of the continent in which the Location occurs. | ... | ... |
| 2 | [higherGeography](https://dwc.tdwg.org/terms/#dwc:higherGeography){:target='_blank'} | A list (concatenated and separated) of geographic names less specific than the information captured in the locality term. | ... | ... |
| 2 | [country](https://dwc.tdwg.org/terms/#dwc:country){:target='_blank'} | The name of the country or major administrative unit in which the Location occurs.| Pays<br> Land | ... |
| 2 | [stateProvince](https://dwc.tdwg.org/terms/#dwc:stateProvince){:target='_blank'} | The name of the next smaller administrative region than country (state, province, canton, department, region, etc.) in which the Location occurs. | ... |
| 2 | [locality](https://dwc.tdwg.org/terms/#dwc:locality){:target='_blank'} | The specific description of the place. | Lieu<br> Fundort | ... |
| 2 | [decimalLatitude](https://dwc.tdwg.org/terms/#dwc:decimalLatitude){:target='_blank'} | The geographic latitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive. | coordonnées x<br> coordinates | ...  |
| 2 | [decimalLongitude](https://dwc.tdwg.org/terms/#dwc:decimalLongitude){:target='_blank'} | The geographic longitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive. | coordonnées y<br> coordinates | ...  |
| 2 | [verbatimElevation](https://dwc.tdwg.org/terms/#dwc:verbatimElevation){:target='_blank'} | The original description of the elevation (altitude, usually above sea level) of the Location. | ... | ... |

| MIDS | DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| ---- | --------------- | ---------- | ------------------------------------- | -------- |
| 3 | [county](https://dwc.tdwg.org/terms/#dwc:county){:target='_blank'} | The full, unabbreviated name of the next smaller administrative region than stateProvince (county, shire, department, etc.) in which the Location occurs.  | ... | ... |
| 3 | [verbatimDepth](https://dwc.tdwg.org/terms/#dwc:verbatimDepth){:target='_blank'} | The original description of the depth below the local surface.  | ...    | ... |


## I made a mistake when importing my data into the Data Aggregator, what do I do?

The Data Aggregator has a structure in three different layers (imported data, encoded data and approved data). For each of them, the history of all imported data is kept continuously. Therefore you can simply re-upload your correct dataset, do the correct mapping and encode it again. As long as your catalogNumber data is consistent, the rest is simply updated when importing a dataset with known catalogNumber values.

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Back to Top Button</title>
  <style>
    /* Style for the Back to Top Button */
    #back-to-top {
      position: fixed;
      bottom: 40px;
      right: 120px;
      display: none;
      background-color: #fa5e97;
      color: white;
      text-align: center;
      padding: 5px;
      border-radius: 5px;
      font-size: 18px;
      cursor: pointer;
      z-index: 1000;
      width: 70px; /* Width for the rectangle */
      height: 50px; /* Height for the rectangle */
      line-height: 40px;
    }

    #back-to-top:hover {
      background-color: #fa5e97;
    }
  </style>
</head>

<body>

  <!-- Back to Top Button -->
  <a id="back-to-top" href="#" title="Back to top">Up</a>

  <script>
    // Show or hide the button when scrolling
    window.onscroll = function() {
      scrollFunction();
    };

    function scrollFunction() {
      var backToTopButton = document.getElementById("back-to-top");
      if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
        backToTopButton.style.display = "block";
      } else {
        backToTopButton.style.display = "none";
      }
    }

    // Scroll to the top when the button is clicked
    document.getElementById("back-to-top").addEventListener("click", function(event) {
      event.preventDefault();
      document.body.scrollTop = 0; // For Safari
      document.documentElement.scrollTop = 0; // For Chrome, Firefox, IE, and Opera
    });
  </script>

</body>
</html>