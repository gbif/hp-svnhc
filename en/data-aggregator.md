---
layout: heroImage
title: Data Aggregator
description: Swiss Data Aggregator and tutorials
background: /assets/images/placeholders/moss.jpg
imageLicense: |
  None for this image, but it would normally go here. Markdown is allowed.
height: 50vh
toc: true
---

# Swiss Data Aggregator

More than 90% of the specimens curated in Switzerland are biological or paleontological. For the aggregation and publication of digital information on these specimens, SwissCollNet will collaborate with InfoSpecies and build on the already existing data infrastructure of the Swiss node of GBIF.

InfoSpecies is the umbrella organisation of the national data centers and coordination offices for species promotion. One of the main goals of InfoSpecies is the provision, management and diffusion of species records, which includes natural history collection data.

The long-term objective is to achieve automatised data transfer of collection data to the national aggregator and publication of data on national and international online portals as well as an automatised update of data records.

Source : [Data aggregation in Switzerland](https://swisscollnet.scnat.ch/fr/collection_data/data_aggregation).

<div style="text-align: left; margin-top: 50px; border: 10px solid #fa5e97; padding: 20px;">
  <p><strong>For the Swiss Natural History institutions who wish to publish data on this portal:</strong></p>
  <p style="text-align: center; font-size: 20px;">
    <a href="https://svnhc.hp.gbif-staging.org/en/how-to-publish-data/">How to publish data - Data Aggregator</a>
  </p>
</div>

# FAQs
## Do I have to upload my entire database fields into the Data Aggregator?
There is no need to upload all fields of your database into the Data Aggregator. You can choose to upload only the most important fields. They are the ones that will be available on the SVNHC portal in the Data pages.

To help you select your field, **here is an empty tsv file with the most important Darwin Core terms** required for GBIF (see: [Data quality requirements: Occurrence datasets](https://www.gbif.org/fr/data-quality-requirements-occurrences)). You can put your data in this file and use it for the upload.
<div style="text-align: right;">
    <a href="https://raw.githubusercontent.com/gbif/hp-svnhc/master/downloadFiles/DarwinCoreSelected.tsv" download="DarwinCoreSelected.tsv">
        <button style="padding: 5px 15px; font-size: 14px; cursor: pointer;">Download TSV</button>
    </a>
</div>


## What is Darwin Core?
[Darwin Core](https://dwc.tdwg.org/){:target="_blank"} is a **data standard**, a template to be used when organising data in a database or a table in order to have distinct and **precise fields with a known and fixed information format** in each of them. It has been created as a helping basis to make [FAIR](https://dwc.tdwg.org/ ){:target="_blank"} data.
The direct benefit of the Darwin Core standard is the **high level of compatibility between data from different sources**.


## But my database/dataset is not formatted in Darwin Core, do I have to change everything?
Rest assured, you do not need to change your database/dataset dramatically. The most important thing is to find the easiest and fastest way to adapt your database/dataset to import it in the data aggregator. Here are our 3 most popular suggestions:


<div style="display: flex; justify-content: space-between; align-items: flex-start;">
  <div style="flex: 3; padding-right: 70px;">
    <strong>1) Add 1 entry in your database/dataset (a new line in your excel file for instance) and fill out each field of this entry with the corresponding <a href="https://dwc.tdwg.org/terms/">Darwin Core term</a></strong> (if and only if the content of the field corresponds to the DwC definition). Adapt your data with the other important DwC terms until all of the information you want to export is ready.
  </div>
  <div style="flex: 1;">
    ✅ No extra work of restructuring your database<br>
    ✅ Easily reversed<br>
    ❌ Data as clean as possible<br>
    ❌ Wrong mapping
  </div>
</div>
<br><br>
<div style="display: flex; justify-content: space-between; align-items: flex-start;">
  <div style="flex: 3; padding-right: 70px;">
    <strong>2) Add the <a href="https://dwc.tdwg.org/terms/">Darwin Core terms</a></strong> in your dataset/database as new columns. With the help of scripts and formulas, pick the fields of your database and copy or adapt their values in the DwC fields in a dynamic way.
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
  <div style="flex: 3; padding-right: 70px;">
    <strong>3) Replace the name of your fields with the corresponding <a href="https://dwc.tdwg.org/terms/">Darwin Core term</a></strong> after checking your field compatibilities with the DwC terms definitions.
  </div>
  <div style="flex: 1;">
    ✅ Fully Darwin Core compatible dataset/database<br>
    ✅ No more changes in the future<br>
    ❌ Difficult to change habits regarding field names<br>
    ❌ Needs a deep cleaning of the whole database/dataset
  </div>
</div>
<br><br>

## Where can I find the Darwin Core terms description?
On the Darwin Core official website, the [Quick Reference Guide](https://dwc.tdwg.org/terms/) is the easiest to use.

Here are a few of the top-10 most used fields (with link to the quick reference guide page):

| DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| --------------- | ---------- | ------------------------------------- | -------- |
| [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName){:target="_blank"} | The full scientific name, with authorship and date information if known. | Scientific name, nom scientifique, Wissenschaftliche Name, Full name, Nom complet | _Cyclamen hederifolium_ Aiton, _Vulpes vulpes (Linnaeus, 1758)_ |
| [eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target="_blank"} | The date-time or interval when the dwc:Event was recorded. Format: for a precise date: YYYY-MM-DD, for an interval: YYYY-MM-DD/YYYY-MM-DD | date of collect, collection date, date de récolte, Funddatum | August 1903, 01.04.85, 15 VII 1867 |
| [recordNumber](https://dwc.tdwg.org/terms/#dwc:recordNumber){:target="_blank"} | An identifier given to the dwc:Occurrence at the time it was recorded (link between field notes and specimen). | field number, collect number, numéro de récolte, Fundnummer | 2089, ASM-515 |
| [catalogNumber](https://dwc.tdwg.org/terms/#dwc:catalogNumber){:target="_blank"} | A unique identifier for the record within the data set or collection. | Code-barre, Numéro, Barcode, Nummer, Numéro d'inventaire | G00009201, Sheet-2765149 |
| [recordedBy](https://dwc.tdwg.org/terms/#dwc:recordedBy){:target="_blank"} | A list (concatenated and separated) of names of people, groups, or organizations responsible for recording the original dwc:Occurrence. | Collector, collecteur, leg. | RSutter, Gilomen, Ed. Berger |


## Which fields are required/mandatory?

### Minimal mandatory fields of the Data Aggregator

<table style="background-color: rgba(173, 216, 230, 0.2); width: 100%; border-collapse: collapse; border: 1px solid black;">
  <tr>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: rgba(173, 216, 230, 0.4);">DwC term (dwc:)</th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: rgba(173, 216, 230, 0.4);">Definition</th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: rgba(173, 216, 230, 0.4);">Corresponding terms found in datasets</th>
    <th style="text-align: left; vertical-align: middle; border: 1px solid black; padding: 5px; background-color: rgba(173, 216, 230, 0.4);">Examples</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 5px;"><a href="https://dwc.tdwg.org/terms/#dwc:scientificName" target="_blank">scientificName</a></td>
    <td style="border: 1px solid black; padding: 5px;">The full scientific name, with authorship and date information if known.</td>
    <td style="border: 1px solid black; padding: 5px;">Scientific name, nom scientifique, Wissenschaftliche Name, Full name, Nom complet</td>
    <td style="border: 1px solid black; padding: 5px;"><i>Cyclamen hederifolium</i> Aiton, <i>Vulpes vulpes</i> (Linnaeus, 1758)</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 10px;"><a href="https://dwc.tdwg.org/terms/#dwc:catalogNumber" target="_blank">catalogNumber</a></td>
    <td style="border: 1px solid black; padding: 10px;">A unique identifier for the record within the data set or collection.</td>
    <td style="border: 1px solid black; padding: 10px;">Code-barre, Numéro, Barcode, Nummer, Numéro d’inventaire</td>
    <td style="border: 1px solid black; padding: 10px;">G00009201, Sheet-2765149</td>
  </tr>
</table>

### Minimal highly recommanded fields of GBIF.org

| DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| --------------- | ---------- | ------------------------------------- | -------- |
| [occurrenceID](https://dwc.tdwg.org/terms/#dwc:occurrenceID){:target="_blank"} | An identifier for the dwc:Occurrence (as opposed to a particular digital record of the dwc:Occurrence). In the absence of a persistent global unique identifier, construct one from a combination of identifiers in the record that will most closely make the dwc:occurrenceID globally unique. | <absent>, automatically created when transferring the data from the Data Aggregator to GBIF.org | 3168574668 |
| [basisOfRecord](https://dwc.tdwg.org/terms/#dwc:basisOfRecord){:target='_blank'} | The specific nature of the data record. | type | Controlled vocabulary:  PreservedSpecimen, FossilSpecimen, LivingSpecimen, HumanObservation, MachineObservation |
| [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName){:target='_blank'}  | The full scientific name, with authorship and date information if known. When forming part of a dwc:Identification, this should be the name in lowest level taxonomic rank that can be determined. This term should not contain identification qualifications, which should instead be supplied in the dwc:identificationQualifier term. | Scientific name, nom scientifique, Wissenschaftliche Name, Full name, Nom complet | _Cyclamen hederifolium_ Aiton, _Vulpes vulpes_ (Linnaeus, 1758) |
| [eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target='_blank'} | The date-time or interval during which a dwc:Event occurred. For occurrences, this is the date-time when the dwc:Event was recorded. Not suitable for a time in a geological context. | date of collect, collection date, date de récolte, Funddatum, date, Datum | August 1903, 01.04.85, 15 VII 1867 |

### MIDS0 fields in the Data Aggregator

| DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| --------------- | ---------- | ------------------------------------- | -------- |
| [catalogNumber](https://dwc.tdwg.org/terms/#dwc:catalogNumber){:target='_blank'} | A unique identifier for the record within the data set or collection. | Code-barre, Numéro, Barcode, Nummer, Numéro d’inventaire | G00009201, Sheet-2765149 |
| [institutionCode](https://dwc.tdwg.org/terms/#dwc:institutionCode){:target='_blank'} | The name (or acronym) in use by the institution having custody of the object(s) or information referred to in the record. <br> See the [GrSciColl official institution codes](https://scientific-collections.gbif.org/institution/search?country=CH){:target="_blank"} | <if you have an example, please do not hesitate to send it to us> | BERN, G, MHNN |

### MIDS1 fields in the Data Aggregator

| DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| --------------- | ---------- | ------------------------------------- | -------- |
| _not DwC_ | Part or parts of the organism that have been preserved. | <if you have an example, please do not hesitate to send it to us> | shell, skeleton, skull, soft tissue |
| [preparations](https://dwc.tdwg.org/terms/#dwc:preparations){:target='_blank'} | A list (concatenated and separated) of preparations and preservation methods for a specimen. | <if you have an example, please do not hesitate to send it to us> | fossil, cast, photograph, DNA extract, skin, skull, skeleton, whole animal (ETOH), tissue (EDTA) |
| [scientificName](https://dwc.tdwg.org/terms/#dwc:scientificName){:target='_blank'} | The full scientific name, with authorship and date information if known. When forming part of an Identification, this should be the name in lowest level taxonomic rank that can be determined. This term should not contain identification qualifications, which should instead be supplied in the IdentificationQualifier term. | Scientific name, nom scientifique, Wissenschaftliche Name, Full name, Nom complet | _Cyclamen hederifolium_ Aiton, _Vulpes vulpes_ (Linnaeus, 1758) |
| [taxonID](https://dwc.tdwg.org/terms/#dwc:taxonID){:target='_blank'} | An identifier for the set of taxon information (data associated with the Taxon class). May be a global unique identifier or an identifier specific to the data set. | <if you have an example, please do not hesitate to send it to us> | 8fa58e08-08de-4ac1-b69c-1235340b7001, 32567, https://www.gbif.org/species/212 |

### MIDS2 fields in the Data Aggregator

| DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| --------------- | ---------- | ------------------------------------- | -------- |
| [eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target='_blank'} | The date-time or interval during which a dwc:Event occurred. For occurrences, this is the date-time when the dwc:Event was recorded. Not suitable for a time in a geological context. | date of collect, collection date, date de récolte, Funddatum, date, Datum | August 1903, 01.04.85, 15 VII 1867 |
| [recordedBy](https://dwc.tdwg.org/terms/#dwc:recordedBy){:target='_blank'} | A list (concatenated and separated) of names of people, groups, or organizations responsible for recording the original Occurrence. The primary collector or observer, especially one who applies a personal identifier (recordNumber), should be listed first. | leg., collecteur, Sammler, collector  | <if you have an example, please do not hesitate to send it to us> |
| [identificationID](https://dwc.tdwg.org/terms/#dwc:identificationID){:target='_blank'} | An identifier for the Identification (the body of information associated with the assignment of a scientific name). May be a global unique identifier or an identifier specific to the data set. | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [taxonID](https://dwc.tdwg.org/terms/#dwc:taxonID){:target='_blank'} | The unique identifier assigned to the organism during a given identification event. | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us> |
| [typeStatus](https://dwc.tdwg.org/terms/#dwc:typeStatus){:target='_blank'} | A list (concatenated and separated) of nomenclatural types (type status, typified scientific name, publication) applied to the subject. | type | <if you have an example, please do not hesitate to send it to us> |
| [continent](https://dwc.tdwg.org/terms/#dwc:continent){:target='_blank'} | The name of the continent in which the Location occurs. | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [country](https://dwc.tdwg.org/terms/#dwc:country){:target='_blank'} | The name of the country or major administrative unit in which the Location occurs.| Pays, Land | <if you have an example, please do not hesitate to send it to us> |
| [county](https://dwc.tdwg.org/terms/#dwc:county){:target='_blank'} | The full, unabbreviated name of the next smaller administrative region than stateProvince (county, shire, department, etc.) in which the Location occurs.  | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [decimalLatitude](https://dwc.tdwg.org/terms/#dwc:decimalLatitude){:target='_blank'} | The geographic latitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive. | coordonnées x, coordinates | <if you have an example, please do not hesitate to send it to us>  |
| [decimalLongitude](https://dwc.tdwg.org/terms/#dwc:decimalLongitude){:target='_blank'} | The geographic longitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive. | coordonnées y, coordinates | <if you have an example, please do not hesitate to send it to us>  |
| [higherGeography](https://dwc.tdwg.org/terms/#dwc:higherGeography){:target='_blank'} | A list (concatenated and separated) of geographic names less specific than the information captured in the locality term. | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [locality](https://dwc.tdwg.org/terms/#dwc:locality){:target='_blank'} | The specific description of the place. | Lieu, Fundort | <if you have an example, please do not hesitate to send it to us> |
| [stateProvince](https://dwc.tdwg.org/terms/#dwc:stateProvince){:target='_blank'} | The name of the next smaller administrative region than country (state, province, canton, department, region, etc.) in which the Location occurs. | <if you have an example, please do not hesitate to send it to us> |
| [verbatimDepth](https://dwc.tdwg.org/terms/#dwc:verbatimDepth){:target='_blank'} | The original description of the depth below the local surface. | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [verbatimElevation](https://dwc.tdwg.org/terms/#dwc:verbatimElevation){:target='_blank'} | The original description of the elevation (altitude, usually above sea level) of the Location. | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [yearCollectionEntrance](https://dwc.tdwg.org/terms/#dwc:yearCollectionEntrance){:target='_blank'} | The four-digit year of collection entrance of a specimen (earliest year of occurrence in absence of a documented collection event). | <if you have an example, please do not hesitate to send it to us> | <if you have an example, please do not hesitate to send it to us> |
| [collectionCode](https://dwc.tdwg.org/terms/#dwc:collectionCode){:target='_blank'} | The name, acronym, coden, or initialism identifying the collection or data set from which the record was derived.                                                                                                                                                                                                                                                                                                                  | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | collectionCode           |
| [collectionID](https://dwc.tdwg.org/terms/#dwc:collectionID){:target='_blank'}                        | An identifier for the collection or dataset from which the record was derived.                                                                                                                                                                                                                                                                                                                                                     | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | collectionID             |
| [originalNameUsage](https://dwc.tdwg.org/terms/#dwc:originalNameUsage){:target='_blank'}              | The taxon name, with authorship and date information if known, as it originally appeared when first established under the rules of the associated nomenclaturalCode. The basionym (botany) or basonym (bacteriology) of the scientificName or the senior/earlier homonym for replaced names.                                                                                                                                         | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | originalNameUsage        |

### MIDS3 in Data Aggregator

| DwC term (dwc:) | Definition | Corresponding terms found in datasets | Examples |
| --------------- | ---------- | ------------------------------------- | -------- |
| [eventDate](https://dwc.tdwg.org/terms/#dwc:eventDate){:target='_blank'}                                              | The date-time or interval during which a dwc:Event occurred. For occurrences, this is the date-time when the dwc:Event was recorded. Not suitable for a time in a geological context.                                                                                                                                                                                                                                            | date of collect, collection date, date de récolte, Funddatum, date, Datum | August 1903, 01.04.85, 15 VII 1867                                                        | eventDate                |
| [recordedBy](https://dwc.tdwg.org/terms/#dwc:recordedBy){:target='_blank'}                                            | A list (concatenated and separated) of names of people, groups, or organizations responsible for recording the original Occurrence. The primary collector or observer, especially one who applies a personal identifier (recordNumber), should be listed first.                                                                                                                                                                     | leg., collecteur, Sammler, collector                                 | <if you have an example, please do not hesitate to send it to us>                          | recordedBy               |
| [identificationID](https://dwc.tdwg.org/terms/#dwc:identificationID){:target='_blank'}                                | An identifier for the Identification (the body of information associated with the assignment of a scientific name). May be a global unique identifier or an identifier specific to the data set.                                                                                                                                                                                                                                   | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | identificationID         |
| [taxonID](https://dwc.tdwg.org/terms/#dwc:taxonID){:target='_blank'}                                                  | The unique identifier assigned to the organism during a given identification event.                                                                                                                                                                                                                                                                                                                                              | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | taxonID                  |
| [typeStatus](https://dwc.tdwg.org/terms/#dwc:typeStatus){:target='_blank'}                                            | A list (concatenated and separated) of nomenclatural types (type status, typified scientific name, publication) applied to the subject.                                                                                                                                                                                                                                                                                           | type                                                                 | <if you have an example, please do not hesitate to send it to us>                          | typeStatus               |
| [continent](https://dwc.tdwg.org/terms/#dwc:continent){:target='_blank'}                                              | The name of the continent in which the Location occurs.                                                                                                                                                                                                                                                                                                                                                                          | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | continent                |
| [country](https://dwc.tdwg.org/terms/#dwc:country){:target='_blank'}                                                  | The name of the country or major administrative unit in which the Location occurs.                                                                                                                                                                                                                                                                                                                                               | Pays, Land                                                          | <if you have an example, please do not hesitate to send it to us>                          | country                  |
| [county](https://dwc.tdwg.org/terms/#dwc:county){:target='_blank'}                                                    | The full, unabbreviated name of the next smaller administrative region than stateProvince (county, shire, department, etc.) in which the Location occurs.                                                                                                                                                                                                                                                                         | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | county                   |
| [decimalLatitude](https://dwc.tdwg.org/terms/#dwc:decimalLatitude){:target='_blank'}                                  | The geographic latitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are north of the Equator, negative values are south of it. Legal values lie between -90 and 90, inclusive.                                                                                                                                                         | coordonnées x, coordinates                                          | <if you have an example, please do not hesitate to send it to us>                          | decimalLatitude          |
| [decimalLongitude](https://dwc.tdwg.org/terms/#dwc:decimalLongitude){:target='_blank'}                                | The geographic longitude (in decimal degrees, using the spatial reference system given in geodeticDatum) of the geographic center of a Location. Positive values are east of the Greenwich Meridian, negative values are west of it. Legal values lie between -180 and 180, inclusive.                                                                                                                                             | coordonnées y, coordinates                                          | <if you have an example, please do not hesitate to send it to us>                          | decimalLongitude         |
| [higherGeography](https://dwc.tdwg.org/terms/#dwc:higherGeography){:target='_blank'}                                  | A list (concatenated and separated) of geographic names less specific than the information captured in the locality term.                                                                                                                                                                                                                                                                                                         | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | higherGeography          |
| [locality](https://dwc.tdwg.org/terms/#dwc:locality){:target='_blank'}                                                | The specific description of the place.                                                                                                                                                                                                                                                                                                                                                                                            | Lieu, Fundort                                                       | <if you have an example, please do not hesitate to send it to us>                          | locality                 |
| [stateProvince](https://dwc.tdwg.org/terms/#dwc:stateProvince){:target='_blank'}                                      | The name of the next smaller administrative region than country (state, province, canton, department, region, etc.) in which the Location occurs.                                                                                                                                                                                                                                                                                 | Canton                                                             | <if you have an example, please do not hesitate to send it to us>                          | stateProvince            |
| [verbatimDepth](https://dwc.tdwg.org/terms/#dwc:verbatimDepth){:target='_blank'}                                      | The original description of the depth below the local surface.                                                                                                                                                                                                                                                                                                                                                                    | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | verbatimDepth            |
| [verbatimElevation](https://dwc.tdwg.org/terms/#dwc:verbatimElevation){:target='_blank'}                              | The original description of the elevation (altitude, usually above sea level) of the Location.                                                                                                                                                                                                                                                                                                                                    | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | verbatimElevation        |
| [yearCollectionEntrance](https://dwc.tdwg.org/terms/#dwc:yearCollectionEntrance){:target='_blank'}                    | The four-digit year of collection entrance of a specimen (earliest year of occurrence in absence of a documented collection event).                                                                                                                                                                                                                                                                                                | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | yearCollectionEntrance   |
| [collectionCode](https://dwc.tdwg.org/terms/#dwc:collectionCode){:target='_blank'}                                    | The name, acronym, coden, or initialism identifying the collection or data set from which the record was derived.                                                                                                                                                                                                                                                                                                                  | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | collectionCode           |
| [collectionID](https://dwc.tdwg.org/terms/#dwc:collectionID){:target='_blank'}                                        | An identifier for the collection or dataset from which the record was derived.                                                                                                                                                                                                                                                                                                                                                     | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | collectionID             |
| [originalNameUsage](https://dwc.tdwg.org/terms/#dwc:originalNameUsage){:target='_blank'}                              | The taxon name, with authorship and date information if known, as it originally appeared when first established under the rules of the associated nomenclaturalCode. The basionym (botany) or basonym (bacteriology) of the scientificName or the senior/earlier homonym for replaced names.                                                                                                                                         | <if you have an example, please do not hesitate to send it to us>    | <if you have an example, please do not hesitate to send it to us>                          | originalNameUsage        |
| [verbatimChronometricAge](https://dwc.tdwg.org/terms/#dwc:verbatimChronometricAge){:target='_blank'}                  | The verbatim age for a specimen, whether reported by a dating assay, associated references, or legacy information.                                                                                                                                                                                                                                                                                                                | <if you have an example, please do not hesitate to send it to us>    | <if you have an
