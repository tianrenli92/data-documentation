---
layout: default
title: Edge Properties
nav_order: 5
---

# Edge Properties
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

Edges (or relationships) contain important properties with details about the relationships between nodes. They also serve as useful parameters for constructing customized queries on the CHCD. Below is information on the properties available for edges. When constructing queries, it is important to remember that not _all_ edges will have _all_ properties listed below.

---

## Edge Properties

| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
| **rel_type** | A short descriptor detailing the relationship between the two nodes. No standard format, but the descriptor follows the directionality of the relationship (e.g., (Matteo Ricci)-[Superior]->(Vice-Province of China), etc.). | STRING |
| **start_day** | Start day of relationship. | INTEGER |
| **start_month** | Start month of relationship. | INTEGER |
| **start_year** | Start year of relationship. | INTEGER |
| **end_day** | End day of relationship. | INTEGER |
| **end_month** | End month of relationship. | INTEGER |
| **end_year** | End year of relationship. | INTEGER |
| **notes** | Additional information about individual. No standard format. | STRING |
| **source** | Source(s) of information. Separated by semicolons. See documentation on [CHCD Sources](../6_sources/) for more information. | STRING |
