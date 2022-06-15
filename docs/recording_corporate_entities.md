---
layout: default
title: Recording Corporate Entities
nav_order: 6
---

# Recording Corporate Entities
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

Corpoarte Entities are an important kind of node within the China Historical Database (CHCD). As a node in the database, corporate enties provide structures of belonging that link instituions and people together in hierchical, non-hierachical, and non-geographical ways. Further, corporate entities are typically used for framing academic fields (e.g. Jesuit Studies, Methodist Studies, etc.), and this means that they can be uased as units of analysis within the database.

This documentation provides guidelines to help you format your own data collection sheets so that the data can be readily cleaned and inputted into the CHCD. Each section provides a description of what is being recorded, a general format for how to record, and examples.

### Defining a Corporate Entity in the CHCD.
 In the CHCD, an *corporate entity* is defined as any Christian organization which cannot reasonably be assigned a geographic location (i.e. a fixed latitude and longitude) and which exists over an extended period of time. Typical examples include denominations, dioceses, mission sending agencies, and administrative divisions within an orgnization. This definition sets them apart from [Institutions](/data-collection/docs/recording_institutions) (which can be assigned a geographic location) and [Events](/data-collection/docs/recording_events) (which do not tend to exist over an extended period of time). If there is any confusion on how to categorize an organization, please contact the CHCD project team.

>*Note: These general formats are suggestions for use in your own data collection, however, please refer to [Data Collection Basics](/data-collection/docs/data_collection_basics/) before designing your own spreadsheets.*

---

## Identifying Static Properties
These are general properties which are recorded non-relationally in the database. They are *identifying* because they are generally unique to each corporate entity.

Below is a list of identifying static properties which should be recorded if your historical document contains them.

---

### abbreviation
Text

#### FORMAT
{: .no_toc }
```
Abbreviation
```
#### EXAMPLES
{: .no_toc }
```
MEC-YC
SJ
```

---

### historical_alternate_abbreviation
Text

#### FORMAT
{: .no_toc }
```
Abbreviation
```
#### EXAMPLES
{: .no_toc }
```
MX-YC
SI
```

---
### name_western
The official or most common English name of the corporate entity or a reasonable English translation.

#### FORMAT
{: .no_toc }
```
Corporate Entity Name
```
#### EXAMPLES
{: .no_toc }
```
Yunnan Conference of the Methodist Episcopal Church
The Society of Jesus
```
---

### alternative_name_western
Alternate names in English or other Western  (e.g. Latin, Dutch, etc.). List common spellings and alternate names that the institution is recorded under.  If listing more than one name, use a semicolon to separate the entries. Separate the names by a semicolon.

#### FORMAT
{: .no_toc }
```
Alternative Name; Alternative Name; ...
```
#### EXAMPLES
{: .no_toc }
```
Methodist New Connection Yunnan Conference
Societas Iesu; Jesuits
```
---
### chinese_name_romanized
Chinese name of the corporate entity in Romanized script, pinyin first followed by any other spelling system. Alternative spellings with a semicolon. Designate the romanization system by abbreviation when possible.

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
Corporate Entity Name (system); Corporate Entity Name (system); ...
```
#### EXAMPLES
{: .no_toc }
```
Mei yi mei hui yun nan hui yi (py)
Yesu hui (py)
```
---

### chinese_alternate_name_romanized
Alternate Chinese names, including different spellings, under which the corporate entity is recorded. If listing more than one name, use a semicolon to separate the entries. Designate the romanization system by abbreviation when possible.

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
Wei li gong hui xin lian jie yun nan hui yi (py)
Yesu hui jiao fu (py)
```
---

### chinese_name_hanzi
The most official or most common Chinese name of the corporate entity, typed in *traditional* (i.e. non-simplified) characters [繁體字].

#### FORMAT
{: .no_toc }
```
法人實體名稱
```
#### EXAMPLES
{: .no_toc }
```
美以美會雲南會議
耶穌會
```
---

### chinese_alternative_name_hanzi
Alternate Chinese names used by the corporate entity. Alternate names should be types in *traditional* (i.e. non-simplified) characters.

#### FORMAT
{: .no_toc }
```
法人實體名稱; 法人實體名稱; ...
```
#### EXAMPLE
{: .no_toc }
```
衛理新連雲南會議
耶穌會教父
```
---

### china_start_date
List the date on which the corporate entity began work in China. Use the Gregorian calendar in the following order, separated by semicolon: day; month; year. If only a Chinese lunar calendar date is available to you, use a [calendrical concordance](https://sinocal.sinica.edu.tw/) to convert it to the Gregorian calendar.

>*Note: If only a year or month is available, you may leave off more specific date components.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLES
{: .no_toc }
```
1860; 05
1583
```
---

### china_end_date
List the date on which the corporate entity ceased work in China. Use the Gregorian calendar in the following order, separated by semicolon: day; month; year. If only a Chinese lunar calendar date is available to you, use a [calendrical concordance](https://sinocal.sinica.edu.tw/) to convert it to the Gregorian calendar. If the organization is still act

>*Note: If only a year or month is available, you may leave off more specific date components. If the corporate entity is still in existence and active in China, then use the value "active" to denote its continuing presence.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLES
{: .no_toc }
```
1939
active
```
---

### nationality
If the corporate entity was affiliated with people from a specific area, list the modern nation-state which occupies the same geographic location as the birthplace of those individuals. If the organization was international in composition, "International" can be provided as a value.

#### FORMAT
{: .no_toc }
```
Country
```
#### EXAMPLES
{: .no_toc }
```
United States of America
International
```
---

### corporate_entity_category
This property records the kind of corporate entity being recorded. These properties are a set list, but more specific categorization can be achieved with the [corporate_entity_subcategory](#corporate_entity_subcategory) property.  

Currently, this property has three potential values:
- **Voluntary Association** = Used to denote organizations such as goodwill societies, charitable associations, etc.
- **Military** = Used to designate the military and paramilitary groups which explicitly identify as Christian.
- **Religious Body** = Used to denote to ecclessiastical, parachurch, and mission organizations.
- **Administrative Subunit** = Used to denoate administrative divisions within a broader organization.

#### FORMAT
{: .no_toc }
```
Type
```
#### EXAMPLES
{: .no_toc }
```
Administrative Subunit
Religious Body
```
---

### corporate_entity_subcategory
This property describes the specific type of the corporate entity being recorded. There is not currently a set list of values, but it is best practice to follow the descriptors of historical documents. If multiple subcategories can be used, separate them using a semicolon.

#### FORMAT
{: .no_toc }
```
Subcategory
```
#### EXAMPLES
{: .no_toc }
```
Mission Conference
Roman Catholic Order
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
Run mostly by Methodists from Pennsylvania.
Supressed between 1773 and 1813.
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
These are general properties which describe the religious identity of a corporate entity. They are *classifying* because they allow institutions to be organized according to standard forms of religious belonging.

Below is a list of classifying static properties which should be recorded if your historical document contains them.

---

### christian_tradition
This property records the broad Christian tradition to which the institution belonged. Institutional belonging can be dictated the by religious belonging of individuals at the institution or by property rights and usage (e.g. a Protestant-identified group owned the building).

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
This property records the subgrouping to which an institution belonged.

For Protestants this includes groupings such as: Lutheran, Methodist, Baptist etc. For Catholics, this includes groupings within a common general tradition, rule, or order, such as: Augustinian, Benedictine, Franciscan, Ignatian, etc. These large ‘regular’ orders were often composed of subgroups (e.g. Discalced Augustinians, Observant Friars Minor, Reformed Friars Minor, etc.). Groups which do not generally fall into a clearly defined family can be labeled as "Independent"

#### FORMAT
{: .no_toc }
```
Religious Family
```
#### EXAMPLES
{: .no_toc }
```
Methodist
Ignatian
```
---

## Relationships
Corporate Entity nodes can have three kinds of relationships in the CHCD:
- [**PART_OF**](#part_of): This links Person, Institution, and Event nodes to Corporate Entity nodes.
- [**CONNECTED_TO**](#connected_to): This links Corporate Entity nodes to other Corporate Entity nodes.

These three categories are devised so as to offer a range of flexibility in recording different types of relationships, while also providing a framework to organize them. When designing your spreadsheet and recording data, it is good to keep these basic relationships in mind. Below are descriptions of each relationships and an example of how it  might be recorded in a spreadsheet.

---

### PART_OF
Typically, this is used to connect a person, institution, or corporate entity to its organizational hierarchy (i.e. to corporate entity nodes). For Protestants, this usually records the specific denomination, missionary body, mission administrative division, or sending agency (e.g. the Church Missionary Society, the True Jesus Church, the South China Conference of the Assemblies of God, etc.) to which an institution or person belonged. For Catholics and Orthodox, this usually indicate the specific diocese, province, or vicarate that an institution or person belonged to (e.g. Luan Diocese, Vice Province of China, etc.)

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the institution's relationship to the corporate entity
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

This property is most commonly used to capture hierarchies of administration (e.g. a church is part of a diocese, a mission is part of a conference, etc.). As historical sources may not include all of this data, it is important to adapt one's spreadsheet to fit the nature of the source for the sake of efficiency. When entering data, make it clear in table headings which kind of data is being collected in the column.

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
MEC South China Conference; Member
Diocese of Luan; Church; 1920; 1935
```
---

### CONNECTED_TO
This is used to connect corporate entities to other corporate entities. Besides making it possible to construct organizational hierarchies, this relationship also allows researchers to denote partnerships or collaborations between organizations.

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the institution's relationship to the corporate entity
- ```start_year``` : Records the starting year of the relationship, also used if no end date to the relationship is available.
- ```start_month``` : Records the starting month of the relationship, also used if no end date to the relationship is available.
- ```start_day``` : Records the starting day of the relationship, also used if no end date to the relationship is available.
- ```end_year``` : Records the ending year of the relationship.
- ```end_month``` : Records the ending year of the relationship.
- ```end_day``` : Records the ending year of the relationship.
- ```note``` : Records any additional information about the relationship.
- ```source``` : Records the source in which the relationship is attested.

#### NOTE ON COLLECTING CONNECTED_TO RELATIONSHIPS
{: .no_toc }

This relationship is most commonly used to capture hierarhies of administration (e.g. a diocese is part of an archdiocese, a mission conference is part of a mission agency, etc.). As historical sources may not include all of this data, it is important to adapt one's spreadsheet to fit the nature of the source for the sake of efficiency. When entering data, make it clear in table headings which kind of data is being collected in the column.

Also, it is important to remember that all relationships in the CHCD are directional. This is especially important for CONNECTED_TO relationships, which tend to run in only one direction (e.g. X is a subunit of Y, but Y is not a subunit of X). Please keep this in mind as you record your data.

Lastly, the CHCD project team maintains a running list of abbreviations for the most common Christian organizations in operation in China throughout the time period of the project. [This list can be found here.](https://docs.google.com/spreadsheets/d/1uhnh-WsTL6cu-kHndIVEBQpXGOLv6Cq6XVPuQ5YhUos/edit?usp=sharing) Please feel free to use these abbreviations to help your data entry be more efficient.

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Corporate Entity; Relationship Type
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
MEC China Mission; Subunit of
Archdiocese of Taiyuan; Subunit of
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
