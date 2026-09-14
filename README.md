# Malacca Ritual Alliance Sites Database

## 1. Introduction

This repository provides a CSV-based geographical database of religious sites associated with ritual alliances and temple networks in Malacca (Melaka), Malaysia. Centred on Cheng Wah Keong Temple (清华宫), it records site names, coordinates, ritual connections, deities, and contextual notes. The dataset supports mapping and the study of cooperation between temples, religious communities, and local organisations.

The current dataset contains **27 records and seven fields**, covering sites in Malacca city and surrounding areas, including Umbai, Telok Mas, Serkam, Tiang Dua, and Bemban. It includes active temples, worship spaces within clan associations, and a historical temple recorded as no longer extant. It is a selected research dataset rather than a complete inventory of religious sites in Malacca.

The main reference is Josephine Fong Xin De's (方欣德) master's thesis, *A Study on the Ritual Alliance of Cheng Wah Keong Temple, Malacca* (《马六甲清华宫仪式联盟研究》, 2026). Site locations and additional information have subsequently been supplemented through online searches and researcher revisions.

## 2. Coordinates and Location Accuracy

`Longitude` and `Latitude` are recorded in decimal degrees, using **WGS84 (EPSG:4326)** as the intended coordinate reference system. All coordinate values are rounded to **four decimal places**. This represents a numerical resolution of approximately 11 metres in latitude at Malacca, but does not establish the accuracy of the underlying location.

Coordinates identify mapped site locations and may represent a building, entrance, or approximate historical location. For temples within clan-association buildings, a point represents the shared building rather than the precise position of an internal shrine. Geocoding methods and source accuracy may differ between records; coordinates have not all been verified through field surveys.

The record for **Geok Hua Keong (玉华宫)** refers to a former temple in Ujong Pasir. Its coordinate should be treated as an approximate historical location requiring further verification, rather than as a currently operating temple. Its Note field records the subsequent worship of Bai Fu Wang Ye at Yong Chuan Tian.

For GIS import, use **Longitude as X** and **Latitude as Y**, and select EPSG:4326. Blank coordinates in future versions should remain null rather than being replaced with zero.

## 3. Fields

The data file is [`Malacca Ritual Alliance Sites.csv`](Malacca%20Ritual%20Alliance%20Sites.csv).

| Field | Description |
|---|---|
| `Chinese Name` | Chinese name of the religious site. |
| `English Name` | Romanised name or English identifier used in the dataset. Romanisation conventions vary; some entries use a locality as an identifier. |
| `Longitude` | Longitude in decimal degrees, rounded to four decimal places. |
| `Latitude` | Latitude in decimal degrees, rounded to four decimal places. |
| `Ritual Alliance` | One or more ritual alliances, procession connections, or organisational networks associated with the site. |
| `Deities` | Deities recorded for the site, including affiliated or transferred worship where specified. This is not necessarily a complete list or a list restricted to principal deities. |
| `Note` | Additional context, such as a clan-association setting, cemetery association, or historical change. Empty or omitted trailing values indicate that no note is supplied. |

### 3.1 Site Names

Chinese names and romanised names provide complementary identifiers. Similar names should not be merged automatically: **Umbai Long Chuan Kong (龙泉宫)** and **Serkam Long Chuan Temple (龙泉庙)** are separate sites. **Telok Mas Wu Wang Gong (五王宫)** is a temple name, whereas **五府王爷联盟** denotes a relationship between multiple temples and deities.

Some identifiers remain provisional. For example, the English Name for 威圣宫 is currently `Tiang Dua`, a locality name. Such entries should be checked before being used as standard temple names.

### 3.2 Ritual Alliances and Networks

The `Ritual Alliance` field preserves the research labels in the CSV. These labels describe several kinds of relationship:

| Label in the CSV | Interpretation |
|---|---|
| 五府王爷联盟 | Five Wang Ye alliance, linking temples and worship associated with the Zhu, Wen, Chi, Li, and Bai Wang Ye. Five deities do not imply five surviving independent temples. |
| 五营联盟 | Five Camps ritual network, involving ritual personnel, spirit-medium practices, and cooperation between temples. |
| 青云亭托管网络 | Cheng Hoon Teng trusteeship network: an administrative and organisational relationship that should be distinguished from joint ritual participation. |
| 2017年清华宫南巡联盟 | Sites associated with Cheng Wah Keong's 2017 southern procession. The dated label records an event connection and does not by itself establish permanent alliance membership. |
| 朱府王爷绕境联盟 | Sites grouped under the dataset's Zhu Fu Wang Ye procession label. The field does not specify the year, route, or duration of each connection. |
| 兴化分灵联盟 | Xinghua-related network of affiliated deity worship, including the Zhu Fu Wang Ye affiliation recorded at Poh Onn Kong. |
| 兴化分香联盟 | Xinghua-related incense-sharing and worship network. |

A site may have several connections. These labels are research categories, not necessarily the official names of registered organisations. They should not be assumed to describe relationships that all existed at the same time.

### 3.3 Deities

Deity names are retained in Chinese to preserve the distinctions used in the source material and dataset. A recorded deity may be a principal deity, an additional deity, or a deity associated with an affiliated shrine. For example, the entry `朱府王爷（分灵）` at Poh Onn Kong describes affiliated worship and should not be read as identifying the temple's principal deity.

Both `Ritual Alliance` and `Deities` contain multiple values separated by English (`;`) or Chinese (`；`) semicolons, sometimes with surrounding spaces. Split on both separator types and trim whitespace when processing these fields. The value `青云亭公托管网络` in the Poh San Teng record appears to be a spelling variant of `青云亭托管网络`; confirm this before merging categories.

## 4. Sources and Compilation

### 4.1 Main Research Reference

Fong, Josephine Xin De (方欣德). 2026. *A Study on the Ritual Alliance of Cheng Wah Keong Temple, Malacca* (《马六甲清华宫仪式联盟研究》). Master's thesis, Xiamen University.

Relevant printed pages include:

- **p. 1 and pp. 51–55:** the Five Wang Ye temples, alliance relations, and Cheng Hoon Teng's organisational role.
- **p. 4 and pp. 62–64:** the Five Camps network and related temples.
- **pp. 37–40:** Xinghua communities, affiliated worship, and incense-sharing connections.
- **pp. 68–69, Tables 5–6:** participants and stops in the 2017 procession.
- **p. 53, footnotes:** temples under Cheng Hoon Teng's trusteeship.

In the supplied PDF, printed page 1 corresponds to PDF page 18. Printed page references should be distinguished from viewer page numbers.

### 4.2 Location References and Researcher Supplements

Earlier location research used public mapping records, temple websites, and local heritage or travel directories. Examples include [Waze's Cheng Wah Keong record](https://www.waze.com/live-map/directions?to=place.ChIJOQz442bu0TER3NcyT0vC2TY), [Mapcarta's Wah Teck Keong record](https://mapcarta.com/W1422283014), [Heng Ann Tian Hou Temple information](https://www.malaysia-traveller.com/heng-ann-tian-hou-temple.html), and [Lian Puan Kiong's published GPS information](https://www.gbs2u.com/bd/index3.asp?idno=6&lang=&userid=19916048).

The current CSV incorporates subsequent revisions and supplements. It does not yet contain record-level source citations, verification dates, or confidence ratings. The examples above document part of the compilation process; they do not establish the provenance of every current coordinate, deity, or alliance label. Additions such as Poh San Teng and Phek Chin Keong should receive explicit source documentation as the database develops.

## 5. Using and Extending the Database

The CSV can be imported into GIS software to map sites, compare the spatial distribution of deities, or examine connections between temples. For network analysis, treat sites as nodes and the recorded alliances or networks as relationship categories. Sharing a label indicates a recorded connection to that category; it does not automatically establish a direct relationship between every pair of sites.

The current table is a flat-file database. Future versions could introduce stable site IDs and separate tables for sites, deities, alliances, and sources, with relationship tables recording dates, roles, and supporting evidence. This would allow historical changes and overlapping memberships to be represented more precisely.

Corrections and additions should include the site name, location evidence, source reference, and the date or event to which an alliance connection applies. Preserve former names and historical locations where they matter to the research.

The organisation of this README follows the introduction, coordinate guidance, field descriptions, and source documentation used in [Historical Religious Sites in Chengdu](https://github.com/Ziyu177147/Historical-Religious-Sites-in-Chengdu).
