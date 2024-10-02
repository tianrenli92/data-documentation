---
layout: default
title: Getting Started
nav_order: 2
---

# Getting Started with the CHCD
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

Unlike traditional relational databases, the CHCD runs on the [Neo4j](https://neo4j.com/) graph database platform. Specifically, it utilizes the free-to-use [Community Edition](https://neo4j.com/download-center/#community). Below are detailed instructions which explain how to download the CHCD CSV data and how to turn it into an operable Neo4j database.

---

## Download CHCD CSVs

CSV files are a widely used and flexible storage option for large datasets. AS such, the CHCD team chose to distribute our database in this format so it can be easily adapted for multiple use-cases. We have also placed it in a Github repository so it is accessible to the general public.

[Download CHCD CSVs](https://github.com/chcdatabase/data){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }

---

## Setting Up the CHCD with CSV Files

The CHCD CSV files can be used in many different applications. However, if you would like to setup a local Neo4j version of the CHCD, follow the below set of instructions.

- **Download CHCD CSV**: See above.
- **Download and Install Neo4j**: Follow these [instructions](https://neo4j.com/docs/desktop-manual/current/installation/download-installation/) to download and install the Neo4j desktop client.
- **Create a Database**: Follow these [instructions](https://neo4j.com/docs/desktop-manual/current/operations/create-dbms/) to create a blank graph database. *Note*: Do not start the graph database. If a database has been started, it will interfere with the importation of CSV data.
- **Move the CHCD CSVs**: Use the three dot menu icon to open up the import folder (See image below). Place `chcd-v-1-nodes.csv` and `chcd-v-1-rels.csv` into this folder.
  <p style="text-align: center;">
  <img src="https://raw.githubusercontent.com/chcdatabase/data-documentation/gh-pages/assets/images/import.png" width="350" style="border: 2px black solid"/>
  </p>
- **Run CSV Import Command**: Use the three dot menu icon to open up the terminal for the database (See image below).
  <p style="text-align: center;">
  <img src="https://raw.githubusercontent.com/chcdatabase/data-documentation/gh-pages/assets/images/terminal.png" width="350" style="border: 2px black solid" />
  </p>
Once the terminal is open, run the following commands.
```
cd bin
```
```
neo4j-admin database import full --multiline-fields=true --delimiter=@ --nodes=import/chcd_v2.3_nodes.csv --relationships=import/chcd_v2.3_edges.csv
```
- **Start Database**: Press the `Start` button to start the database.
  <p style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/d54cd6e2-3c62-4376-b187-722482e5dbef" width="350" style="border: 2px black solid"/>
  </p>
- **Open Database**: Press the `Open` button to open the database. You can also use [Neo4j Bloom](https://neo4j.com/docs/bloom-user-guide/current/) to visualize it.
  <p style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/02700d1b-a5f9-44d5-91c4-2898aaef3846" width="350" style="border: 2px black solid"/>
  </p>
  <p style="text-align: center;">
  <img src="https://github.com/user-attachments/assets/1bd5abf4-84ac-4706-90a4-d977095f0713" width="350" style="border: 2px black solid"/>
  </p>

---

## Neo4j & Cypher

Users must utilize the Cypher language to write queries in Neo4j. Neo4j maintains a full suite of documentation and training to help new users learn the basics of graph databases in general, Neo4j in particular, and the Cypher query language.

- [Getting Started with Neo4j Resources](https://neo4j.com/developer/getting-started-resources/)
- [Free GraphAcademy Neo4j Courses](https://graphacademy.neo4j.com/)
- [Neo4j Desktop Manual](https://neo4j.com/docs/desktop-manual/current/)
- [Neo4j Cypher Manual](https://neo4j.com/docs/cypher-manual/current/)
