---
layout: default
title: API
nav_order: 7
---

# Connecting to the CHCD via API
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

The Neo4j graph platform includes a API so that outside applications can access a database more easily. The information below will help you if you are interested in integrating CHCD data with your project.

---

## Neo4j API Drivers

Neo4j officially supports API drivers for .Net, Java, JavaScript, Go, and Python. The Neo4j community maintains drivers for all other major coding languages. These drivers enable Neo4j's Bolt protocol and allow applications to run Cypher queries. For more information on API drivers and how to integrate them into your project, read [Neo4j's Drivers and Language Guide](https://neo4j.com/developer/language-guides/).

---

## Credentials

Connections to the database via API allows projects to run queries on the database. With such a large dataset, these queries can become expensive if not monitored. As such, the CHCD team controls access to the API by providing account credentials to our partners. If you are interested in integrating the CHCD into your project via an API, reach out to the [Project Team](alex.mayfield@asbury.edu).

---

## Properties & Example Query

As a graph database, information is stored in both nodes and relationships. Queries will likely need to utilize both in order to retrieve useful results. While the CHCD does include geographic nodes, the primary nodes of interest in the database have the following labels: `:Person`, `:Institution`, `:CorporateEntity`, and `:Event`. For more information about the various node labels and relationship types in the database. See the [Node Properties Documentation](/docs/4_node_properties) and the [Edge Properties Documentation](/docs/5_edge_properties).

For example, many projects may be interested in a specific group of people within a specific time frame. If a project was interested in retrieving all the Portuguese individuals between 1600 and 1700 in the database, they might write a query like this:

```
MATCH (n:Person {nationality: "Portugal"})-[t]-(q)
WHERE t.start_year >= 1600 AND t. start_year <= 1700
      OR t.end_year >=1600 AND t.end_year <=1700
      OR n.birth_year >= 1600 AND n.birth_year <= 1700
      OR n.death_year >= 1600 AND n.death_year <= 1700  
RETURN n,t,q
```

Let's break down this simple query.
```
MATCH (n:Person {nationality: "Portugal"})-[t]-(q)
```  
This first section matches any `:Person` node in the database that has the nationality of "Portugal" and that has a relationship with any other node.  
```
WHERE t.start_year >= 1600 AND t. start_year <= 1700
      OR t.end_year >=1600 AND t.end_year <=1700
      OR n.birth_year >= 1600 AND n.birth_year <= 1700
      OR n.death_year >= 1600 AND n.death_year <= 1700
```  
The second section narrows the results down to only include nodes which have dates between 1600 and 1700. The `WHERE` clause checks the `t` relationship properties and `n` node properties and includes any node that has a date which falls between the time period.  
```
RETURN n,t,q
```  
This final section returns the nodes and relationships. Most use cases will likely require that that data return is in a specific format. This can be accomplished easily with the `RETURN` clause. For more information on how to manipulate returned data, see the Neo4j's [RETURN Clause Documentation](https://neo4j.com/docs/cypher-manual/current/clauses/return/).

It is likely that you may need a different or more complex sort of query for your application. If this is the case, be sure to consult this documentation and the [Neo4j Cypher Manual](https://neo4j.com/docs/cypher-manual/current/).
