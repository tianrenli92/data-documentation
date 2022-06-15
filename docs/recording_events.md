---
layout: default
title: Recording Events
nav_order: 7
---

# Recording Events
{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>
---

## Introduction

Event nodes are a unique addition to the China Historical Database (CHCD) which allows the database to capture moments of interaction which might otherwise be lost. Because of their importance, the database has numerous properties which can be used to record information about them.

This documentation provides guidelines to help you format your own data collection sheets so that the data can be readily cleaned and inputted into the CHCD. Each section provides a description of what is being recorded, a general format for how to record, and examples.

### Defining an Event in the CHCD.
 In the CHCD, an *event* is defined as any historical happening which can reasonably be assigned a geographic location(s), but which does not exist over an extended period of time. This definition sets them apart from [Corporate Entities](/data-collection/docs/recording_corporate_entities) (which lack the ability to be assigned a geographic location) and [Institutions](/data-collection/docs/recording_institutions) (which do tend to exist over an extended period of time).

As a category, "event" is a rather broad term. It can include things like important revivals, conferences, evangelistic trips, or even publications. If there is any confusion on how to categorize an organization, please contact the CHCD project team.

>*Note: These general formats are suggestions for use in your own data collection, however, please refer to [Data Collection Basics](/data-collection/docs/data_collection_basics/) before designing your own spreadsheets.*

---

## Identifying Static Properties
These are general properties which are recorded non-relationally in the database. They are *identifying* because they are generally unique to each event.

Below is a list of identifying static properties which should be recorded if your historical document contains them.

---

### name_western
The official or most common English name of the event or a reasonable English translation.

#### FORMAT
{: .no_toc }
```
Event Name
```
#### EXAMPLES
{: .no_toc }
```
Siege of the International Legations
The True Meaning of the Lord of Heaven
```
---

### alternative_name_western
Alternate names in English or other Western  (e.g. Latin, Dutch, etc.). List common spellings and alternate names that the event is recorded under.  If listing more than one name, use a semicolon to separate the entries. Separate the names by a semicolon.

#### FORMAT
{: .no_toc }
```
Alternative Name; Alternative Name; ...
```
#### EXAMPLES
{: .no_toc }
```
Siege of the Foreign Legations Quarter
Lord of Heaven
```
---
### chinese_name_romanized
Chinese name of the event in Romanized script, pinyin first followed by any other spelling system. Alternative spellings with a semicolon. Designate the romanization system by abbreviation when possible.

Here is a list of the most common romanization systems utilized with suggested abbreviation:

- *(py)*: Hanyu pinyin
- *(wg)*: Wade-Giles
- *(y)*: Yale
- *(lsw)*: Latinhua Sin Wenz
- *(gr)*: Gwoyeu Romatzyh (National Romanization)
- *(j2)*: Juyin II
- *(po)*: Chinese Post Office System
- *(rt)*: Ricci-Trigault System
- *(ef)*: Système de l'École Française d'Extrême-Orient

#### FORMAT
{: .no_toc }
```
Event Name (system); Event Name (system); ...
```
#### EXAMPLES
{: .no_toc }
```
Wei gong guo ji gong shi guan (py)
Tian zhu shi yi (py)
```
---

### chinese_alternate_name_romanized
Alternate Chinese names, including different spellings, under which the event is recorded. If listing more than one name, use a semicolon to separate the entries. Designate the romanization system by abbreviation when possible.

Here is a list of the most common romanization systems utilized with suggested abbreviation:

- *(py)*: Hanyu pinyin
- *(wg)*: Wade-Giles
- *(y)*: Yale
- *(lsw)*: Latinhua Sin Wenz
- *(gr)*: Gwoyeu Romatzyh (National Romanization)
- *(j2)*: Juyin II
- *(po)*: Chinese Post Office System
- *(rt)*: Ricci-Trigault System
- *(ef)*: Système de l'École Française d'Extrême-Orient

#### FORMAT
{: .no_toc }
```
Alternative Name (system); Alternative Name (system);
```
#### EXAMPLE
{: .no_toc }
```
Wei gong guo ji gong shi guan qu (py)
Tian zhu (py)
```
---

### chinese_name_hanzi
The most official or most common Chinese name of the event, typed in *traditional* (i.e. non-simplified) characters [繁體字].

#### FORMAT
{: .no_toc }
```
機構名稱
```
#### EXAMPLES
{: .no_toc }
```
圍攻國際公使館
天主實義
```
---

### chinese_alternative_name_hanzi
Alternate Chinese names used by the event. Alternate names should be types in *traditional* (i.e. non-simplified) characters.

#### FORMAT
{: .no_toc }
```
機構名稱; 機構名稱; ...
```
#### EXAMPLE
{: .no_toc }
```
圍攻外國使館區
天主
```
---

### start_date
List the start date of the event using the Gregorian calendar in this order, separated by semicolon: day; month; year. If only a Chinese lunar calendar date is available to you, use a [calendrical concordance](https://sinocal.sinica.edu.tw/) to convert it to the Gregorian calendar.

>*Note: If only a year or month is available, you may leave off more specific date components.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLES
{: .no_toc }
```
1920; 06; 20
1603
```
---

### end_date
List the end date of the event using the Gregorian calendar in this order, separated by semicolon: day; month; year. If only a Chinese lunar calendar date is available to you, use a [calendrical concordance](https://sinocal.sinica.edu.tw/) to convert it to the Gregorian calendar.

>*Note: If only a year or month is available, you may leave off more specific date components. Publications do not have end dates.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLES
{: .no_toc }
```
1900; 08; 14

```
---

### event_category
This property records the kind of event which took place. These properties are a set list.

Currently, this property has four potential values:
- **Journey** = Used for events such as evangelistic tours, diplomatic journeys, sea voyages, etc.
- **Meeting** = Used for events such as conferences, revivals, important religious services, etc.
- **Publication** = Used for publications of any kind.
- **Conflict** = Used for events which involved violence, such as a battle, massacre, riot, etc.

#### FORMAT
{: .no_toc }
```
Type
```
#### EXAMPLES
{: .no_toc }
```
Conflict
Publication
```
---

### event_subcategory
This property records the specific type of the event being recorded. There is not currently a set list of values, but it is best practice to follow the descriptors of historical documents. If multiple subcategories can be used, separate them using a semicolon.

#### FORMAT
{: .no_toc }
```
Subcategory; Subcategory; ...
```
#### EXAMPLES
{: .no_toc }
```
Siege
Book; Apologetic
```
---

## Documentational Static Properties
These are documentational properties which are recorded non-relationally in the database. They are *documentational* because they record additional notes and source material.

Below is a list of documentational static properties which should be recorded if your historical document contains them.

---

### notes
Add any additional pertinent information that cannot be recorded any of the other static categories. There is no standardized format for this property.

#### FORMAT
{: .no_toc }
```
No set format.
```
#### EXAMPLE
{: .no_toc }
```
Part of the Boxer Rebellion.
The first Chinese Christian text of the early-modern period.
```
---

### source
List the sources where the information in this table has been found, followed by page number in parenthesis. Indicate first major reference sources used, then more focused sources if some specific information is not in main reference sources (indicate what). Sources can be indicated in abbreviated form or with acronyms (e.g *Dehergne Repertoire*, 159).

#### FORMAT
{: .no_toc }
```
Source Information [Page #]; Source Information [Page #];
```
#### EXAMPLE
{: .no_toc }
```
Eugenio Menegon, “Ricci, Francesco,” in  Dizionario biografico degli Italiani, vol X, Roma, Istituto Treccani, 2016 [XX]; For name in Chinese see ARSI, Japonica Sinica XXX [XX]
```
---

## Classifying Properties
These are general properties which describe the religious belonging of an event. They are *classifying* because they allow events to be organized according to standard forms of religious belonging.

Below is a list of classifying static properties which should be recorded if your historical document contains them.

>*Note: Within the database, classifying properties are generally connected to or describe [Corporate Entities](/data-collection/docs/recording_corporate_entities) (i.e. institutions derive their classification through their connection to corporate entities). They are included here, however, as it may be useful in your own workflow for data collection.*

---

### christian_tradition
This property records the broad Christian tradition to which an event belonged. Event belonging can be dictated the by religious belonging of individuals at the event or by property rights and usage (e.g. the event took place at a building owned by a Protestant-identified group).

This property has three potential values:
- **Protestant**
- **Catholic**
- **Orthodox**

#### FORMAT
{: .no_toc }
```
Tradition
```
#### EXAMPLES
{: .no_toc }
```
Protestant
Catholic
```
---

### religious_family
This property records the subgrouping to which an event belonged.

For Protestants this includes groupings such as: Lutheran, Methodist, Baptist etc. For Catholics, this includes groupings within a common general tradition, rule, or order, such as: Augustinian, Benedictine, Franciscan, Ignatian, etc. These large ‘regular’ orders were often composed of subgroups (e.g. Discalced Augustinians, Observant Friars Minor, Reformed Friars Minor, etc.). Use the [religious_body](#religious_body) property to define the precise group. Groups which do not generally fall into a clearly defined family can be labeled as "Independent"

Event belonging can be dictated the by religious belonging of individuals at the event or by property rights and usage (e.g. the event took place at a building owned by a Methodist-identified group). Events which had more than one religious family participating can be recorded as "Ecumenical."


#### FORMAT
{: .no_toc }
```
Religious Family
```
#### EXAMPLES
{: .no_toc }
```
Ecumenical
Ignatian
```
---

### religious_body
This property records the specific organization to which an event belonged. For Protestants, this could denote a specific denomination, missionary organization, or sending agency (e.g. United Methodist Church, China Inland Mission, Young Men's Christian Association, etc.) For Catholics, this indicates the specific religious order or sending agency (e.g. Discalced Carmelites; Society of Jesus; Propaganda Fide, etc.). Events which had more than one religious body participating can be recorded as "Interdenominational."

#### FORMAT
{: .no_toc }
```
Religious Body
```
#### EXAMPLES
{: .no_toc }
```
Interdenominational
Society of Jesus
```
---

## Relationships
Event nodes can have three kinds of relationships in the CHCD:
- [**PART_OF**](#part_of): This links Person, Institution, and Event nodes to Corporate Entity nodes.
- [**PRESENT_AT**](#present_at): This links Person nodes to Institution or Event nodes.
- [**LOCATED_IN**](#located_in): This links Event nodes to Geography nodes.
- [**LINKED_TO**](#linked_to): This links Event nodes and Institution nodes to each other.

These three categories are devised so as to offer a range of flexibility in recording different types of relationships, while also providing a framework to organize them. When designing your spreadsheet and recording data, it is good to keep these basic relationships in mind. Below are descriptions of each relationships and an example of how it  might be recorded in a spreadsheet.

---

### PART_OF
Typically, this is used to connect an event to its organizational sponsor (i.e. to corporate entity nodes). For Protestants, this usually records the specific denomination, missionary body, mission administrative division, or sending agency (e.g. the Church Missionary Society, the True Jesus Church, the South China Conference of the Assemblies of God, etc.) to which an institution belonged. For Catholics and Orthodox, this usually indicate the specific diocese, province, or vicarate that an event was sponsored by (e.g. Luan Diocese, Vice Province of China, etc.)

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the event's relationship to the corporate entity
- ```start_year``` : Records the starting year of the relationship, also used if no end date to the relationship is available.
- ```start_month``` : Records the starting month of the relationship, also used if no end date to the relationship is available.
- ```start_day``` : Records the starting day of the relationship, also used if no end date to the relationship is available.
- ```end_year``` : Records the ending year of the relationship.
- ```end_month``` : Records the ending year of the relationship.
- ```end_day``` : Records the ending year of the relationship.
- ```note``` : Records any additional information about the relationship.
- ```source``` : Records the source in which the relationship is attested.

#### NOTE ON COLLECTING PART_OF RELATIONSHIPS
{: .no_toc }

This property is most commonly used to indicate the primary sponsor of an event. As historical sources may not include all of this data, it is important to adapt one's spreadsheet to fit the nature of the source for the sake of efficiency. When entering data, make it clear in table headings which kind of data is being collected in the column.

Also, it is important to remember that all relationships in the CHCD are directional. This is especially important for PART_OF relationships, which tend to run in only one direction (e.g. X is part of Y, but Y is not part of X). Please keep this in mind as you record your data.

Lastly, the CHCD project team maintains a running list of abbreviations for the most common Christian organizations in operation in China throughout the time period of the project. [This list can be found here.](https://docs.google.com/spreadsheets/d/1uhnh-WsTL6cu-kHndIVEBQpXGOLv6Cq6XVPuQ5YhUos/edit?usp=sharing) Please feel free to use these abbreviations to help your data entry be more efficient.

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Corporate Entity; Relationship Type; Start YYYY; End YYYY
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
China Inland Mission; Sponsored by
Diocese of Luan; Funded by
```
---

### PRESENT_AT
This relationship category is used to connect People to Institutions and Events, and thus to record where they were located in China (see note below).

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the person's relationship to the institution or event.
- ```start_year``` : Records the starting year of the relationship, also used if no end date to the relationship is available.
- ```start_month``` : Records the starting month of the relationship, also used if no end date to the relationship is available.
- ```start_day``` : Records the starting day of the relationship, also used if no end date to the relationship is available.
- ```end_year``` : Records the ending year of the relationship.
- ```end_month``` : Records the ending year of the relationship.
- ```end_day``` : Records the ending year of the relationship.
- ```note``` : Records any additional information about the relationship.
- ```source``` : Records the source in which the relationship is attested.

#### NOTE ON COLLECTING PRESENT_AT RELATIONSHIPS
{: .no_toc }

As historical sources may not include all of this data, it is important to adapt one's spreadsheet to fit the nature of the source for the sake of efficiency. When entering data, make it clear in table headings which kind of data is being collected in the column.

Please remember, in the CHCD, geography is controlled by allowing only institutions and events to have geographic locations (For more on this design choice, see [Database Design](/data-collection/docs/database_design/) and [Geography]/data-collection/docs/geography/). As such, persons are not directly linked to geographic nodes in the database. Due to this, one should use placeholder institutions when a person is present in a location, but is not institutionally affiliated. For more on the correct formatting of placeholder institutions, see [Placeholder Institutions](/data-collection/docs/geography/#placeholder-institutions).

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Event; Relationship Type; Start MM/YYYY; End MM/YYYY; Note
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
Siege of the Foreign Legation Quarter; Participant; 06/1900; 07/1900; Died during the siege.
The True Meaning of the Lord of Heaven; Author
```
---

### LOCATED_IN
This relationship is among the most important in the database and connects an institution or event to a geography node. More colloquially, this is how the database records the location of an event or institution. In the database, this relationship enables these nodes (and people who are connected to them) to be connected to geographic coordinates.

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```start_year``` : Records the starting year of the relationship, also used if no end date to the relationship is available.
- ```start_month``` : Records the starting month of the relationship, also used if no end date to the relationship is available.
- ```start_day``` : Records the starting day of the relationship, also used if no end date to the relationship is available.
- ```end_year``` : Records the ending year of the relationship.
- ```end_month``` : Records the ending year of the relationship.
- ```end_day``` : Records the ending year of the relationship.
- ```note``` : Records any additional information about the relationship.
- ```source``` : Records the source in which the relationship is attested.

#### NOTE ON COLLECTING LOCATED_IN RELATIONSHIPS
{: .no_toc }
Historical locations in China can, at times, be difficult to locate depending on the nature of the source and the location in question.Various romanization systems, shifting adminstrative divisions, and changing names can make locating historical sources difficult. For this reason, the CHCD has chosen to always record the place name as listed in a historical source.

At the same time, the CHCD uses a [Geography System](/data-collection/docs/geography) that corresponds to a modern administrative map of China. While limited, this use of the multi-level geography system allows us to capture historical geographic data that is precise to varying degrees. As such, when collecting data, it is a best practice to relate the historic location to its most specific modern equivalent and include the corresponding CHCD geography code.

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Event; Historic Place Name; Modern Location; Geocode
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
Siege of the Foreign Legation Quarter; Peking; Dongcheng District; C2502
The True Meaning of the Lord of Heaven; Peking; Dongcheng District; C2502
```
---

### LINKED_TO
This can be used to connect Event nodes to other Event nodes or Institution nodes. Importantly, this means "linked to" in the broadest sense of the word.

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the institution's relationship to the other institution.
- ```start_year``` : Records the starting year of the relationship, also used if no end date to the relationship is available.
- ```start_month``` : Records the starting month of the relationship, also used if no end date to the relationship is available.
- ```start_day``` : Records the starting day of the relationship, also used if no end date to the relationship is available.
- ```end_year``` : Records the ending year of the relationship.
- ```end_month``` : Records the ending year of the relationship.
- ```end_day``` : Records the ending year of the relationship.
- ```note``` : Records any additional information about the relationship.
- ```source``` : Records the source in which the relationship is attested.

#### NOTE ON COLLECTING LINKED_TO RELATIONSHIPS
{: .no_toc }

It is important to remember that all relationships in the CHCD are directional. Sometimes, this directionality is meaningless (e.g. X is a partner institution to Y and Y is a partner institution to X), but sometimes it means that the ```relationship_type``` property is true in only one direction (e.g. X is hosted by Y, but Y is not hosted by X). Please keep this in mind as you record your data.

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Temporary ID of Event 1; Relationship Type; Temporary ID of Event 2
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
I023; Hosted by; I035
I024; Sequel to; I120
```
---

## Example Spreadsheets
As stated throughout, make sure to design your spreadsheet to work most efficiently with your source materials. That said, it can be helpful to see examples of spreadsheets in action.

### SPREADSHEET 1: SINGLE PERSON RESEACH
{: .no_toc }
This sort of spreadsheet might be useful if you are inputting data from a personal archive or biography.

[Spreadsheet 1](https://docs.google.com/spreadsheets/d/10BuoT-fsqqMzPzTqRK-T_U4nrzBxgcirkVBls2bBFvw/edit?usp=sharing){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

### SPREADSHEET 2: MULTI-PERSON RESEARCH
{: .no_toc }
This sort of spreadsheet might be useful if you are working through a institutional archive, necrology, or specialized directory.

[Spreadsheet 2](https://docs.google.com/spreadsheets/d/1Z-Buq3Hjz9y0sQziInQlaaauqSWTJWWu0j2BC4YW_WI/edit?usp=sharing){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
