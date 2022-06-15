---
layout: default
title: Recording People
nav_order: 4
---

# Recording People
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

People are the most numerous kind of node in the China Historical Database (CHCD). As such, the database has numerous properties which can be used to record information about people. This documentation provides guidelines to help you format your own data collection sheets so that the data can be readily cleaned and inputted into the CHCD.

Most of these properties cannot be conceptualized as a relationship. However, the CHCD team chose to record some relational data as static properties. This choice was made to ensure that future queries of the data did not become too complex or worse, meaningless.

Each section provides a description of what is being recorded, a general format for how to record, and examples.

>*Note: These general formats are suggestions for use in your own data collection, however, please refer to [Data Collection Basics](/data-collection/docs/data_collection_basics/) before designing your own spreadsheets.*

---

## Identifying Static Properties
These are general properties which are recorded non-relationally in the database. They are *identifying* because they refer primarily to a person's personal identity and life-events.

Below is a list of identifying static properties which should be recorded if your historical document contains them.

---

### name_western
Western language name; in the native language of the individual, if possible. For individuals with multiple names, use the name given at birth, if possible. If the birth name is not available, use the most well known name. Separate family and given name with a comma.

>*Note: This property will be divided into two properties when put into the database (family_name_western; given_name_western). They are combined here for data entry efficiency.*

#### FORMAT
{: .no_toc }
```
Family Name, Given Name(s)
```
#### EXAMPLES
{: .no_toc }
```
Ricci, Vittorio Giovanni Battista
Song, John
```
---

### alternative_name_western
Alternate names in other Western languages (e.g. Latin, Dutch, etc.). List common spellings and alternate names that the individual is recorded under.  If listing more than one name, use a semicolon to separate the entries. Separate the names by a semicolon.

#### FORMAT
{: .no_toc }
```
Alternative Name; Alternative Name
```
#### EXAMPLES
{: .no_toc }
```
Victorio Riccio; Victorius Riccius
Sung, John
```
---

### chinese_name_romanized
Chinese name in Romanized script, pinyin first followed by any other spelling system. Separate family and given name with a comma. Alternative spellings with a semicolon. Designate the romanization system by abbreviation when possible.

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

>*Note: This property will be divided into two properties when put into the database (chinese_family_name_romanized; chinese_given_name_romanized). They are combined here for data entry efficiency.*

#### FORMAT
{: .no_toc }
```
Family, Given Name (system); Family, Given Name (system);
```
#### EXAMPLES
{: .no_toc }
```
Li, Sheng (py)
Shang, Jie (py); Siong, Ceh (unknown)
```
---

### chinese_alternate_name_romanized
Alternate Chinese names, including different spellings, under which the individual is recorded. These include the Chinese courtesy name (zi), alternative name (hao) and other courtesy or honorific names (See, [chinese_alternative_name_hanzi](# chinese_alternative_name_hanzi) for more types). If listing more than one name, use a semicolon to separate the entries. Designate the romanization system by abbreviation when possible.

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
Tian En
```
---

### chinese_name_hanzi
The family name [姓] and given name [名] of an individual, typed in *traditional* (i.e. non-simplified) characters [繁體字]. Separate the names with a comma.

>*Note: This property will be divided into two properties when put into the database (chinese_family_name_hanzi; chinese_given_name_hanzi). They are combined here for data entry efficiency.*

#### FORMAT
{: .no_toc }
```
姓, 名
```
#### EXAMPLES
{: .no_toc }
```
利, 勝
宋, 尚節
```
---

### chinese_alternative_name_hanzi
Include any zi [字] or hao [號]，or other Chinese alternate names utilized by the individual, followed by the type in parenthesis. Alternate names should be types in *traditional* (i.e. non-simplified) characters, and *pinyin* should be used to record the type.

A list of the most common name types is below:
- *xing [姓]*: family names
- *xiaozi/xioaming [小字/小名]*: childhood name
- *ming [名]*: given name
- *zi [字]*: courtesy name
- *hao [號]*: self-selected alternative name
- *chuohao [綽號]*: nickname given by others
- *guanzhi/guanjue [官職/官爵]*: office names
- *shihao [諡號]*: posthumous title granted by state
- *zunhao [尊號]*: honorific name granted by others
- *miahao [廟號]*: temple title

#### FORMAT
{: .no_toc }
```
字(zi); 號(hao)
```
#### EXAMPLE
{: .no_toc }
```
天恩 (xiaozi)
```
---

### gender
Use the following notation to record the gender of an individual:

- **M** = Male
- **F** = Female
- **U** = Unknown

---

### nationality
List the modern nation-state which occupies the same geographic location as the birthplace of the individual. Record in English.

#### FORMAT
{: .no_toc }
```
Country
```
#### EXAMPLES
{: .no_toc }
```
Italy
China
```
---

### birth_date
List the date of birth in the Gregorian calendar in this order, separated by semicolon: day; month; year. If only a Chinese lunar calendar date is available to you, use a [calendrical concordance](https://sinocal.sinica.edu.tw/) to convert it to the Gregorian calendar.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLES
{: .no_toc }
```
1917; 02; 13
1901; 09; 21
```
---

### birth_place
List the place of birth. The name of the place is recorded in its original language, as well as its modern English equivalent. If the location is in China, a [Geography Code](/data-collection/docs/geography/#geographic_code_system) is added.

#### FORMAT
{: .no_toc }
```
Recorded Place Name; Modern Place Name; Geography Code
```
#### EXAMPLES
{: .no_toc }
```
Firenze; Florence; --
Wu-Chang; Wuchang District; C451
```
---

### death_date
List the date of death in the Gregorian calendar in this order, separated by semicolon: day; month; year. If only a Chinese lunar calendar date is available to you, use a [calendrical concordance](https://sinocal.sinica.edu.tw/) to convert it to the Gregorian calendar.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLES
{: .no_toc }
```
1917; 02; 13
1944; 08; 18
```
---

### death_place
List the place of death. The name of the place is recorded in its original language, as well as its modern equivalent. If the location is in China, a [Geography Code](/data-collection/docs/geography) is added.

#### FORMAT
{: .no_toc }
```
Original Place Name; Modern Place Name; Geography Code
```
#### EXAMPLES
{: .no_toc }
```
Firenze; Florence; --
Wu-Chang; Wuchang District; C451
```
---

## Descriptive Static Properties
These are descriptive properties which are recorded non-relationally in the database. They are *descriptive* because they refer primarily to affiliations and accomplishments of the person.

Below is a list of descriptive static properties which should be recorded if your historical document contains them.

---

### christian_tradition
List the tradition to which this individual belongs. Use the following notation:

- **P** = Protestant
- **C** = Catholic
- **X** = Orthodox
- **R** = Other

---

### religious_family
List the general Christian family this person belongs to. For Protestants this includes groupings such as: Lutheran, Methodist, Baptist etc.; for Catholics, this includes groupings within a common general tradition or rule such as: Augustinian, Benedictine, Franciscan (these large ‘regular’ orders were often composed of subgroups, e.g. Discalced Augustinians; Observant or Reformed Friars Minor / Franciscans; etc.). If they belong to more than one tradition, separate by semicolon.

#### FORMAT
{: .no_toc }
```
Religious Family; Religious Family
```
#### EXAMPLES
{: .no_toc }
```
Carmelite
Methodist; Holiness
```
---

### degrees
Western state degrees, church degrees, or Chinese examination degrees, followed by the granting institution and the year in which they received the title, if known. If listing more than one degree, use a semicolon to separate the entries.

#### FORMAT
{: .no_toc }
```
Degree, Institution (YYYY); Degree, Institution (YYYY)
```
#### EXAMPLES
{: .no_toc }
```
Lector in Philosophy, Collegial of S. Maria Sopra Minerva College
Bachelor of Arts, Yale University (1905); Masters in Divinity (1910)
```
---

### titles
List all honorary and ecclesial titles obtained by individuals throughout their careers, followed by the year in which they received the title, if known. If listing more than one title, use a semicolon to separate the entries.

#### FORMAT
{: .no_toc }
```
Title (YYYY); Title (YYYY)
```
#### EXAMPLES
{: .no_toc }
```
Apostolic Prefect of Formosa; Apostolic Prefect of Terra Australis (1664)
Reverend (1937)
```
---

### occupations
Occupations held before or during their time in China.  Provide dates, if available. Separate by semicolon if there are more than one jobs.

>*Note: Occupations is used to describe more general work roles or occupations not linked to a specific place or institution. If the location or employing institution is known, see the [PRESENT_AT](#present_at) relationship.*

#### FORMAT
{: .no_toc }
```
Occupation, Employer (YYYY); Occupation, Employer (YYYY)
```
#### EXAMPLES
{: .no_toc }
```
Lecturer; Procurator
Painter; Notary; Author
```
---

## Catholic-Specific Static Properties
These are properties which are recorded non-relationally in the database. They are *Catholic-specific* because they typically are only used by Catholic individuals.

Below is a list of Catholic-specific static properties which should be recorded if your historical document contains them.

---

### baptismal_name_western
Mainly used for Chinese converts and members of religious orders. Record in English.

#### FORMAT
{: .no_toc }
```
Baptismal Name
```
#### EXAMPLE
{: .no_toc }
```
Paul
```
---

### chinese_baptismal_name_romanized
Mainly used for Chinese converts. Chinese baptismal name in Romanized script, pinyin first followed by any other spelling system. Designate the romanization system by abbreviation when possible.

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
xi ming (py)
```
#### EXAMPLE
{: .no_toc }
```
Bao Lu (py)
```
---

### chinese_baptismal_name_hanzi
The baptismal name [洗名] of an individual, typed in *traditional* (i.e. non-simplified) characters [繁體字].

#### FORMAT
{: .no_toc }
```
 洗名
```
#### EXAMPLE
{: .no_toc }
```
保祿
```
---

### originating_province
List the religious province to which the person belonged prior to their arrival in China.

#### FORMAT
{: .no_toc }
```
Originating Province
```
#### EXAMPLE
{: .no_toc }
```
Province of Our Lady of the Most Holy Rosary (Philippines)
```
---

### china_province
List the religious province to which the person belonged during their time in China.

#### FORMAT
{: .no_toc }
```
China Province
```
#### EXAMPLE
{: .no_toc }
```
Vice-Province of China
```
---

### join_date
List the date in which the person joined the order or congregation.

#### FORMAT
{: .no_toc }
```
YYYY; MM; DD
```
#### EXAMPLE
{: .no_toc }
```
1783; 02; --
```
---

### vows
List the vows which the person took and dates, if available. Vows should be separated by semicolons.

#### FORMAT
{: .no_toc }
```
Vow (YYYY); Vow (YYYY)
```
#### EXAMPLE
{: .no_toc }
```
Standard Vows (1834); Fourth Vow (1844)
Simple Vows (1745)
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
Recorded as a notable calligrapher.
Most likely died from cholera.
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

## Relationships
People nodes can have three kinds of relationships in the CHCD:
- [**PART_OF**](#part_of): This links Person, Institution, and Event nodes to Corporate Entity nodes.
- [**PRESENT_AT**](#present_at): This links Person nodes to Institution or Event nodes.
- [**RELATED_TO**](#related_to): This links Person nodes to other Person nodes.

These three categories are devised so as to offer a range of flexibility in recording different types of relationships, while also providing a framework to organize them. When designing your spreadsheet and recording data, it is good to keep these basic relationships in mind. Below are descriptions of each relationships and an example of how it  might be recorded in a spreadsheet.

---

### PART_OF
Typically, this is used to capture the specific religious group that a person belonged to. For Protestants, this usually records the specific denomination, missionary body, mission administrative division, or sending agency (e.g. the Church Missionary Society, the True Jesus Church, the South China Conference of the Assemblies of God, etc.) to which a person belonged. For Catholics and Orthodox, this usually indicate the specific order or province (e.g. Discalced Carmelites, Vice Province of China, etc.) to which a person belonged.

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the person's relationship to the corporate entity
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

As historical sources may not include all of this data, it is important to adapt one's spreadsheet to fit the nature of the source for the sake of efficiency. When entering data, make it clear in table headings which kind of data is being collected in the column.

Also, the CHCD project team maintains a running list of abbreviations for the most common Christian organizations in operation in China throughout the time period of the project. [This list can be found here.](https://docs.google.com/spreadsheets/d/1uhnh-WsTL6cu-kHndIVEBQpXGOLv6Cq6XVPuQ5YhUos/edit?usp=sharing) Please feel free to use these abbreviations to help your data entry be more efficient.

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Religious Body, Relationship Type, Start YYYY
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
MEC, Member (1905)
BeM, Evangelist (1920)
Independent, Evangelist (1932)
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
Institution; Start YYYY; Relationship Type; Recorded Place Name; Modern Place Name; Geography Code; Note
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
Jesuit College of Macao; 1921; Guest; Macau; Macao; C979; Worked as pharmacist while present.
General Area (Shanxi); 1933; Evangelist; Shansi; Shanxi; C979;
```
---

### RELATED_TO
This is used to connect People nodes to People nodes. Importantly, it means "related to" in the broadest sense of the word.

This relationship also has its own properties which can be used to record data about the nature of the relationship. They are as follows:
- ```relationship_type``` : A one or two word descriptor of the person's relationship to the other person
- ```start_year``` : Records the starting year of the relationship, also used if no end date to the relationship is available.
- ```start_month``` : Records the starting month of the relationship, also used if no end date to the relationship is available.
- ```start_day``` : Records the starting day of the relationship, also used if no end date to the relationship is available.
- ```end_year``` : Records the ending year of the relationship.
- ```end_month``` : Records the ending year of the relationship.
- ```end_day``` : Records the ending year of the relationship.
- ```note``` : Records any additional information about the relationship.
- ```source``` : Records the source in which the relationship is attested.

#### NOTE ON COLLECTING RELATED_TO RELATIONSHIPS
{: .no_toc }

All people with recorded relationships will be entered into the database. As such, it is best to record the [Identifying Static Properties](#Identifying Static Properties) of anyone who is recorded in a relationship. This methodical approach allows you to assign temporary ID numbers to individuals. These ID numbers can be used to help record relationships in a more timely manner. See [Example Spreadsheet 2](#spreadsheer_2_mulit-person_research), for an example of this approach.

Also, it is important to remember that all relationships in the CHCD are directional. Sometimes, this directionality is meaningless (e.g. X is Friend to Y and Y is Friend to X), but sometimes it means that the ```relationship_type``` property is true in only one direction (e.g. X is Parent of Y, but Y is not Parent of X). Please keep this in mind as you record your data.

#### EXAMPLE HEADER FORMAT
{: .no_toc }
```
Temporary ID of Person 1; Relationship Type; Temporary ID of Person 1; Start YYYY; End YYYY; Note
```
#### EXAMPLE ENTRIES
{: .no_toc }
```
P023; Married to; P035; 1925; 1943; Spouse died of dysentery.
P024; Married to; P120; 1945
P024; Parent of; P234; 1927
P035; Parent of; P234; 1927
P024; Parent of; P256; 1948
P120; Parent of; P256; 1948
P024; Schoolmate of; P002; --; --; Studied Chinese together.
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
