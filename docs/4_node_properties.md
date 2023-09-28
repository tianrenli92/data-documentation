---
layout: default
title: Node Properties
nav_order: 4
---

# Node Properties
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

Nodes contain the largest array of properties within the database. These properties provide basic information on the major entities within the database. They also serve as useful parameters for constructing customized queries on the CHCD. Below is information on the properties available for each node type. When constructing queries, it is important to remember that not _all_ nodes will have _all_ properties that are available for their node type.

---

## Person Node Properties

| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
| **id** | Unique ID for each node. Prefixed with "P_" | STRING |
| **family_name_western** | Family name of individual. | STRING |
| **given_name_western** | Given name of individual. | STRING |
| **alternative_name_western** | Alternative names of individual that may be found in historical sources. Separated by semicolons. | STRING |
| **chinese_family_name_hanzi** | The family name (姓) of an individual. | STRING |
| **chinese_given_name_hanzi** | The given name (名) of an individual. | STRING |
| **alternative_chinese_name_hanzi** | Alternative Chinese names of individual that may be found in historical sources. Sometimes followed by pinyinized name type in parenthesis. (E.g. (xing), (xiaozi), (zi), (chouhao), (zunhao), (miaohao), etc.). Separated by semicolons. | STRING |
| **chinese_family_name_romanized** | Most common Romanized version of family name (姓) of an individual. | STRING |
| **chinese_given_name_romanized** | Most common Romanized version of given name (名) of an individual. | STRING |
| **alternative_chinese_name_romanized** | Alternative Romanized names of individual that may be found in historical sources. Sometimes followed by abbreviated romanization system in parenthesis. (e.g. (py) for pinyin, (wg) for wade-giles, etc.). Separated by semicolons. | STRING |
| **birth_day** | Day of birth | INTEGER |
| **birth_month** | Month of birth. | INTEGER |
| **birth_year** | Year of birth. | INTEGER |
| **birth_place** | Place of birth. As recorded. No standard format. | INTEGER |
| **death_day** | Day of death. | INTEGER |
| **death_month** | Month of death. | INTEGER |
| **death_year** | Year of death. | INTEGER |
| **death_place** | Place of death. As recorded. No standard format.  | STRING |
| **burial_place** | Place of burial. As recorded. No standard format.  | STRING |
| **gender** | Options: Male, Female, Unknown. | STRING |
| **nationality** | English name of the modern nation-state which occupies the same geographic location as the birthplace of the individual. Current options: Argentina, Australia, Austria, Belarus, Belgium, Brazil, Britain, Canada, Canda, Chile, China, Colombia, Croatia, Czech Republic, Denmark, Egypt, England, Finland, Flanders, France, Germany, Guatemala, Guyana, Haiti, Holland, Hungary, India, International, Ireland, Italy, Japan, Korea, Latvia, Libya, Lithuania, Luxembourg, Macao, Malta, Mexico, Monaco, Myanmar, Netherlands, New Zealand, Norway, Peru, Philippines, Poland, Portugal, Romania, Russia, Scotland, Singapore, Slavonia, Slovakia, Slovenia, Spain, Sweden, Switzerland, Turkey, Ukraine, United States of America, Unknown, Uruguay, Vietnam, Wales, Yugoslavia. | STRING |
| **embarkment** | Date (DD/MM/YYY) and/or place of embarkment. | STRING |
| **title** | Titles associated with individual in historical sources. | STRING |
| **occupation** | Known occupations that cannot be turned into relational data (i.e. "She was a painter."). | STRING |
| **degree** | Known degrees as recorded in historical sources. | STRING |
| **christian_tradition** | Options: Protestant, Catholic, Orthodox, Unknown, Non-Religious. | STRING |
| **religious_family** | Broad Christian tradition to which an individual belonged. Current Options: Non-Religious, Interdenominational, Pentecostal, Adventist, Baptist, Congregational, Quaker, Lutheran, Presbyterian, Anglican, Independent, Methodist, Holiness, Nondenominational, Brethren, Reformed, Restorationist, Mennonite, Dominican, Franciscan, Ignatian, Claretian, Augustinian, Benedictine, Carmelite, Cistercian, Ursuline, Salesian, Russian Orthodoxy, Maryknoll, Latter Day Saints, Passionist. | STRING |
| **baptism** | Date (DD/MM/YYY) and/or place of baptism. | STRING |
| **confirmation** | Date (DD/MM/YYY) and/or place of confirmation (Catholic-specific). | STRING |
| **vestition** | Date (DD/MM/YYY) and/or place of  vestition (Catholic-specific). | STRING |
| **ordination_deacon** | Date (DD/MM/YYY) and/or place of ordination to deaconate (Catholic-specific). | STRING |
| **ordination_priest** | Date (DD/MM/YYY) and/or place of ordination to priesthood (Catholic-specific). | STRING |
| **ordination_bishop** | Date (DD/MM/YYY) and/or place of ordination to bishopric (Catholic-specific). | STRING |
| **ordination_archbishop** | Date (DD/MM/YYY) and/or place of ordination to archbishopric (Catholic-specific). | STRING |
| **beatification** |  Date (DD/MM/YYY) of beatification (Catholic-specific). | STRING |
| **canonization** | Date (DD/MM/YYY) of canonization (Catholic-specific). | STRING |
| **notes** | Additional information about individual. No standard format. | STRING |
| **source** | Source(s) of information. Separated by semicolons. See documentation on [CHCD Sources](../6_sources/) for more information. | STRING |

---

## Institution Node Properties

| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
| **id** | Unique ID for each node. Prefixed with "N_" | STRING |
| **name_western** | Most common English name of institution. | STRING |
| **alternative_name_western** | Alternative names of institution, including translations in other Western languages. Separated by semi-colons. | STRING |
| **chinese_name_hanzi** | Most common Chinese name of institution. | STRING |
| **alternative_chinese_name_hanzi** | Alternative Chinese names of institution. Separated by semi-colons. | STRING |
| **name_romanized** | Most common Romanized name of institution. | STRING |
| **alternative_name_romanized** | Alternative Romanized names of institution. Sometimes followed by abbreviated romanization system in parenthesis. (e.g. (py) for pinyin, (wg) for wade-giles, etc.). Separated by semicolons. | STRING |
| **institution_category** | Category of institution. Current options: Ecclesial, Education, Medical, Other , Rescue, Press, General Area, Other, Scientific, Government. | STRING |
| **institution_subcategory** | Subcategory of institution. Current options: Mission, Seminary, School, Hospital, Community Center, Church, Recreation Club, Higher Education, Missionary Training Home, Missionary Training, Orphanage, Residence, Missionary Home, Bible School, Museum, Blind School, Orphanage for Blind, Mission Press, Military, General Work, Missionary Hostel, Leperosy Asylum, Women's Home, Sanitarium, Children's Work, Industrial Home, Governmental, Leprosy Asylum, Clinic, Dispensary, Internment Camp, Missionary Training Institute, Research, Non-Christian Site, Business, Nursing School, Minor Seminary, Religious Residence, Catechetical School, Language School, Administration, Education, Leper Care. | STRING |
| **nationality** | Nationality of an institution. English name of the modern nation-state which occupies the same geographic location as original nation-state. Current options: Argentina, Australia, Austria, Belarus, Belgium, Brazil, Britain, Canada, Canda, Chile, China, Colombia, Croatia, Czech Republic, Denmark, Egypt, England, Finland, Flanders, France, Germany, Guatemala, Guyana, Haiti, Holland, Hungary, India, International, Ireland, Italy, Japan, Korea, Latvia, Libya, Lithuania, Luxembourg, Macao, Malta, Mexico, Monaco, Myanmar, Netherlands, New Zealand, Norway, Peru, Philippines, Poland, Portugal, Romania, Russia, Scotland, Singapore, Slavonia, Slovakia, Slovenia, Spain, Sweden, Switzerland, Turkey, Ukraine, United States of America, Unknown, Uruguay, Vietnam, Wales, Yugoslavia. | STRING |
| **gender_served** | Options: Male, Female, Mixed, Unknown. | STRING |
| **christian_tradition** | Options: Protestant, Catholic, Orthodox, Unknown, Non-Religious. | STRING |
| **religious_family** | Broad Christian tradition to which an institution belonged. Current Options: Non-Religious, Interdenominational, Pentecostal, Adventist, Baptist, Congregational, Quaker, Lutheran, Presbyterian, Anglican, Independent, Methodist, Holiness, Nondenominational, Brethren, Reformed, Restorationist, Mennonite, Dominican, Franciscan, Ignatian, Claretian, Augustinian, Benedictine, Carmelite, Cistercian, Ursuline, Salesian, Russian Orthodoxy, Maryknoll, Latter Day Saints, Passionist. | STRING |
| **start_day** | Start day of institution. | INTEGER |
| **start_month** | Start month of institution. | INTEGER |
| **start_year** | Start year of institution. | INTEGER |
| **end_day** | End day of institution. | INTEGER |
| **end_month** | End month of institution. | INTEGER |
| **end_year** | End year of institution. | INTEGER |
| **notes** | Additional information about institution. No standard format. | STRING |
| **source** | Source(s) of information. Separated by semicolons. See documentation on [CHCD Sources](../6_sources.md) for more information. | STRING |

---

## Corporate Entity Node Properties

| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
| **id** | Unique ID for each node. Prefixed with "C_" | STRING |
| **name_western** | Most common English name of corporate entity. | STRING |
| **alternative_name_western** | Alternative names of corporate entity, including translations in other Western languages. Separated by semi-colons. | STRING |
| **chinese_name_hanzi** | Most common Chinese name of corporate entity. | STRING |
| **alternative_chinese_name_hanzi** | Alternative Chinese names of corporate entity. Separated by semi-colons. | STRING |
| **name_romanized** | Most common Romanized name of corporate entity. | STRING |
| **alternative_name_romanized** | Alternative Romanized names of corporate entity. Sometimes followed by abbreviated romanization system in parenthesis. (e.g. (py) for pinyin, (wg) for wade-giles, etc.). Separated by semicolons. | STRING |
| **abbreviation** | Abbreviation used within the CHCD to refer to the corporate entity. These try to maintain continuity with historical abbreviations whenever possible. | STRING |
| **other_abbreviation** | Alternate and/or historical abbreviations used to refer to corporate entity. | STRING |
| **corporate_entity_category** | Category of corporate entity. Current options: Medical Body, Religious Body, Educational Body, Administrative Subunit, Publishing Body, Other, Publication, Military. | STRING |
| **corporate_entity_subcategory** | Subcategory of corporate entity. Current options: Medical Association, Missionary Society, Chinese Movement, Publication Society, Educational Association, Auxiliary Organization, Religious Community of Women, Religious Community of Men, Association of Diocesan Right (Chinese Religious Community of Women), Roman Curial Body, Archdiocese, Diocese, Vicariate Apostolic, Prefecture Apostolic, Mission Sui Iuris , Mission Sui Iuris, Apostolic Exarchate, Apostolic Administration, Missionary Journal, Geographic Division, Committee, Department, Denomination, Missioanry Publication, Special Commission, Periodical. | STRING |
| **nationality** | Nationality of an institution. English name of the modern nation-state which occupies the same geographic location as original nation-state. Current options: Argentina, Australia, Austria, Belarus, Belgium, Brazil, Britain, Canada, Canda, Chile, China, Colombia, Croatia, Czech Republic, Denmark, Egypt, England, Finland, Flanders, France, Germany, Guatemala, Guyana, Haiti, Holland, Hungary, India, International, Ireland, Italy, Japan, Korea, Latvia, Libya, Lithuania, Luxembourg, Macao, Malta, Mexico, Monaco, Myanmar, Netherlands, New Zealand, Norway, Peru, Philippines, Poland, Portugal, Romania, Russia, Scotland, Singapore, Slavonia, Slovakia, Slovenia, Spain, Sweden, Switzerland, Turkey, Ukraine, United States of America, Unknown, Uruguay, Vietnam, Wales, Yugoslavia. | STRING |
| **china_start** | Year in which corporate entity began work in China (typically for missionary organizations). | INTEGER |
| **christian_tradition** | Options: Protestant, Catholic, Orthodox, Unknown, Non-Religious. | STRING |
| **religious_family** | Broad Christian tradition to which a corporate entity belonged. Current Options: Non-Religious, Interdenominational, Pentecostal, Adventist, Baptist, Congregational, Quaker, Lutheran, Presbyterian, Anglican, Independent, Methodist, Holiness, Nondenominational, Brethren, Reformed, Restorationist, Mennonite, Dominican, Franciscan, Ignatian, Claretian, Augustinian, Benedictine, Carmelite, Cistercian, Ursuline, Salesian, Russian Orthodoxy, Maryknoll, Latter Day Saints, Passionist. | STRING |
| **start_day** | Start day of corporate entity. | INTEGER |
| **start_month** | Start month of corporate entity. | INTEGER |
| **start_year** | Start year of corporate entity. | INTEGER |
| **end_day** | End day of corporate entity. | INTEGER |
| **end_month** | End month of corporate entity. | INTEGER |
| **end_year** | End year of corporate entity. | INTEGER |
| **notes** | Additional information about corporate entity. No standard format. | STRING |
| **source** | Source(s) of information. Separated by semicolons. See documentation on [CHCD Sources](../6_sources.md) for more information. | STRING |

---

## Event Node Properties

| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
| **id** | Unique ID for each node. Prefixed with "E_" | STRING |
| **name_western** | Most common English name of event. | STRING |
| **alternative_name_western** | Alternative names of event, including translations in other Western languages. Separated by semi-colons. | STRING |
| **chinese_name_hanzi** | Most common Chinese name of event. | STRING |
| **alternative_chinese_name_hanzi** | Alternative Chinese names of event. Separated by semi-colons. | STRING |
| **name_romanized** | Most common Romanized name of event. | STRING |
| **alternative_name_romanized** | Alternative Romanized names of event. Sometimes followed by abbreviated romanization system in parenthesis. (e.g. (py) for pinyin, (wg) for wade-giles, etc.). Separated by semicolons. | STRING |
| **event_category** | Category of event. Current options: Journey, Political Embassy, Missionary Party. | STRING |
| **event_subcategory** | Subcategory of event. Current options: Journey, Missionary Party. | STRING |
| **christian_tradition** | Options: Protestant, Catholic, Orthodox, Unknown, Non-Religious. | STRING |
| **religious_family** | Broad Christian tradition to which an individual belonged. Current Options: Non-Religious, Interdenominational, Pentecostal, Adventist, Baptist, Congregational, Quaker, Lutheran, Presbyterian, Anglican, Independent, Methodist, Holiness, Nondenominational, Brethren, Reformed, Restorationist, Mennonite, Dominican, Franciscan, Ignatian, Claretian, Augustinian, Benedictine, Carmelite, Cistercian, Ursuline, Salesian, Russian Orthodoxy, Maryknoll, Latter Day Saints, Passionist. | STRING |
| **start_day** | Start day of event. | INTEGER |
| **start_month** | Start month of event. | INTEGER |
| **start_year** | Start year of event. | INTEGER |
| **end_day** | End day of event. | INTEGER |
| **end_month** | End month of event. | INTEGER |
| **end_year** | End year of event. | INTEGER |
| **notes** | Additional information about event. No standard format. | STRING |
| **source** | Source(s) of information. Separated by semicolons. See documentation on [CHCD Sources](../6_sources.md) for more information. | STRING |

---

### Publication Node Properties
| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
---

### General Area Node Properties
| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
---

## Geography Node Properties

| KEY | NOTE | TYPE |
|:-----|:-----|:-----|
| **id** | Unique ID for each node. Village nodes prefixed with "V_". Townships nodes prefixed with "T_". County nodes prefixed with "Y_". Prefecture nodes prefixed with "F_". Province nodes prefixed with "O_". Nation nodes prefixed with "A_". | STRING |
| **name_wes**  | English name of modern administrative division (c. 2009). | STRING |
| **name_zh**  | Hanzi name of modern administrative division (c. 2009). | STRING |
| **name_rom**  | Pinyin name of modern administrative division (c. 2009). | STRING |
| **latitude**  | Latitude value of centroid point of modern administrative division (c. 2009). | INTEGER |
| **longitude**  | Longitude value of centroid point of modern administrative division (c. 2009). | INTEGER |
