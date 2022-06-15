---
layout: default
title: Database Design
nav_order: 2
---

# Design of the CHCD
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

The CHCD is a graph database that focuses on geographic and relational connections. It utilizes the open-source and industry leading graph database platform [Neo4j](https://neo4j.com/). This section provides information on graph database basics and the general design of the database itself.

---

## Graph Basics
Graph databases mimic the natural relationships that exist in the real world; their structures often look like what you might draw on a white board when trying to describe how things are related. It is helpful to keep this basic framework in mind when devising spreadsheets for data collection.

The example image and four definitions below offer a basic understanding of the graph database approach:

![Graph Database Example Image](https://raw.githubusercontent.com/chcdatabase/data-collection/gh-pages/assets/images/graph_example.jpg)

### Terminology

- **Nodes**: These are the primary entities of a database. (e.g. Matteo Ricci, Xu Guangqi)
- **Relationships**: Also called "edges." These are the relationships between entities. Relationships in a graph databases tend to be directional (e.g. Clavius taught Ricci, Ricci baptized Xu).
- **Labels**: These are primary markers for a node and a relationship. They also can be used to help communicate a flexible structure to the database. Nodes and relationships can have multiple labels if needed. (e.g. Ricci was a priest like Clavius, Xu was a lay person).
- **Properties**: This is additional information that pertains to a specific node or relationship. This information is not relational and does not change (e.g. Clavius taught Ricci at the Roman College).

---

## Graph Schema
The CHCD has four main kinds of nodes (i.e. four node labels) in the database: ```:Person```, ```:CorporateEntity```, ```:Institution```, and ```Event```. In addition, there are five kinds of geographic nodes which represent the five different levels of geography in the database: ```:Village```, ```:Township```, ```:County```, ```:Prefecture```, and ```:Province```

These four main nodes and five geographic nodes are connected by seven kinds of relationship (i.e. seven edge labels) in the database: ```:PART_OF```, ```:RELATED_TO```, ```:AFFILIATED_WITH```, ```:PRESENT_AT```, ```:LOCATED_IN```, ```:LINKED_TO```, and ```:INSIDE_OF```.

The below schema depicts the overall structure of the database by showing what relationships are possible between the various types of nodes.

![CHCD Graph Database Design](https://raw.githubusercontent.com/chcdatabase/data-collection/gh-pages/assets/images/CHCD_Diagram.jpg)

### Node Descriptions

-```:Person```: these nodes represent human beings. People are at the core of the database and thus they have the most kinds of relationships possible.
- ```:CorporateEntity```: these nodes represent organizations that do not have a direct geographic footprint. For example, the Society of Jesus is an organization, but it only exists in space through people and institutions.
- ```:Institution```: these nodes represent organizations that do have a direct geographic footprint.  Common examples in the database include churches, hospitals, and schools.
- ```:Event```: these nodes represent important events that took place in Chinese Christianity. Events are, by definition, temporary happenings that have specific geographic locations. Examples in the database range from Christian conferences to imperial hunting parties.

### Relationship Descriptions

- ```:PART_OF```: used to connect ```:Institution```, ```:Person```, and ```:Event``` nodes to ```:CorporateEntity``` nodes. Enables the ability to capture administrative hierarchies.
- ```:PRESENT_AT```: used to connect ```:Person``` nodes to ```:Institution``` and ```:Event``` nodes. These relationships are the only way individuals receive geographic location in the database.
- ```:LOCATED_IN```: used to connect ```:Institution``` and ```:Event``` nodes to geography nodes.

- ```:RELATED_TO```: used to connect ```:Person``` nodes to each other. These can capture any sort of interpersonal relationship.
- ```:LINKED_TO```: used to connect ```:Institution``` nodes and ```:Event``` nodes. This can capture any sort of relationship between institutions and/or events.
- ```:CONNECTED_TO```: used to connect ```:CorporateEntity``` nodes to each other. This can capture any sort of relationship between events.
- ```:INSIDE_OF```: used to connect geography nodes to one another. This allows the database to reflect administrative hierarchy and fuzzy geograpahic data.


---

## Implications of Design
The CHCD design schema is a careful balance of flexibility and rigidity. This combination allows for a wide amount of historical data collection without having to alter the core structure of the database. While limiting in some respects, these design choices provide the following benefits.

### Bridges the Catholic-Protestant Divide
{: .no_toc }

While Protestant and Catholic organizational structures are quite different, the flexible database structure of the CHCD allows them to be recorded and analyzed together, something rarely done in the study of Christianity in China.

### Allows for Multiple Forms of Belonging
{: .no_toc }

Christian people moved between institutions, institutions changed locations, and corporate entities often split. The CHCD design makes it easy to track these changes while limiting redundancy.

### Controls Complex and Fuzzy Geographies
{: .no_toc }

Geography is regulated using two principles. First, the only nodes that have geographic coordinates attached to them are geography nodes (i.e. Village, Township, County, Prefecture, Province). Second, the only nodes which can relate to geography nodes are Institution and Event nodes. These principles, in turn, accomplish two main goals: 1) historical locations with varying levels of geographic specificity can be recorded, and 2) redundancy and errors are reduced. For more information, see the documentation on [Geography](/data-collection/docs/geography).

### Easy and Understandable Query
{: .no_toc }

When users download the database and use its native Neo4j environment, they can utilize the easy-to-learn Cypher query language. Complex data schemas can be difficult to write queries for, making it difficult to derive meaningful data. By putting a whole host of historical data into a single, simple schema, researchers can more easily analyze disparate sources.

### Easy to Grow
{: .no_toc }

The four primary node types are not the only kind of historical entities or information that could be placed in a database. While initial data collection will focus on these entities, the graph database structure can grow to include different kinds of information. This future growth will further enrich any data already recorded.
