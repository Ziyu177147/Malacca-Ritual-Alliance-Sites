# Malacca Ritual Alliance Sites Database


## 1. Introduction

This repository provides a CSV-based geographical database of religious sites associated with ritual alliances and temple networks in Malacca (Melaka), Malaysia. Centred on Cheng Wah Keong Temple (清华宫), it records site names, coordinates, ritual connections, deities, and contextual notes. The dataset supports mapping and the study of cooperation between temples, religious communities, and local organisations.

The current dataset contains 27 records and seven fields, covering sites in Malacca city and surrounding areas, including Umbai, Telok Mas, Serkam, Tiang Dua, and Bemban. It includes active temples, worship spaces within clan associations, and a historical temple recorded as no longer extant. It is a selected research dataset rather than a complete inventory of religious sites in Malacca.

The main reference is Josephine Fong Xin De's (方欣德) master's thesis, *A Study on the Ritual Alliance of Cheng Wah Keong Temple, Malacca* (《马六甲清华宫仪式联盟研究》, 2026) and fieldwork materials of the project creator.

## 2. Coordinates and Location Accuracy

`Longitude` and `Latitude` are recorded in decimal degrees, using **WGS84 (EPSG:4326)** as the intended coordinate reference system. All coordinate values are rounded to **four decimal places**. This represents a numerical resolution of approximately 11 metres in latitude at Malacca, but does not establish the accuracy of the underlying location.

The record for **Geok Hua Keong (玉华宫)** refers to a former temple in Ujong Pasir. Its coordinate should be treated as an approximate historical location requiring further verification, rather than as a currently operating temple. Its Note field records the subsequent worship of Bai Fu Wang Ye at Yong Chuan Tian.

## 3. Fields

The data file is [`Malacca Ritual Alliance Sites.csv`](Malacca%20Ritual%20Alliance%20Sites.csv).

| Field             | Description                                                                                                                                                                    |
| ----------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `Chinese Name`    | Chinese name of the religious site.                                                                                                                                            |
| `English Name`    | Romanised name or English identifier used in the dataset. Romanization conventions vary; some entries use a locality as an identifier.                                         |
| `Longitude`       | Longitude in decimal degrees, rounded to four decimal places.                                                                                                                  |
| `Latitude`        | Latitude in decimal degrees, rounded to four decimal places.                                                                                                                   |
| `Ritual Alliance` | One or more ritual alliances, procession connections, or organisational networks associated with the site.                                                                     |
| `Deities`         | Deities recorded for the site, including affiliated or transferred worship where specified. This is not necessarily a complete list or a list restricted to principal deities. |
| `Note`            | Additional context, such as a clan-association setting, cemetery association, or historical change. Empty or omitted trailing values indicate that no note is supplied.        |

### 3.1 Site Names

Chinese names and romanised names provide complementary identifiers. Similar names should not be merged automatically: **Umbai Long Chuan Kong (龙泉宫)** and **Serkam Long Chuan Temple (龙泉庙)** are separate sites. **Telok Mas Wu Wang Gong (五王宫)** is a temple name, whereas **五府王爷联盟** denotes a relationship between multiple temples and deities.

### 3.2 Ritual Alliances and Networks

The `Ritual Alliance` field preserves the research labels in the CSV. These labels describe several kinds of relationship:

| Label in the CSV | Interpretation                                                                                                                                                                                                                                                                                                                                                                                                                |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 五府王爷联盟           | Five Wang Ye alliance, linking temples and worship associated with the Zhu, Wen, Chi, Li, and Bai Wang Ye.                                                                                                                                                                                                                                                                                                                    |
| 五营联盟             | Five Camps ritual alliance, involving ritual personnel, spirit-medium practices, and cooperation between temples.                                                                                                                                                                                                                                                                                                             |
| 青云亭托管网络          | Cheng Hoon Teng trusteeship network: an administrative and organisational relationship that should be distinguished from joint ritual participation.                                                                                                                                                                                                                                                                          |
| 2017年清华宫南巡联盟     | Sites associated with Cheng Wah Keong's 2017 southern procession. The dated label records an event connection and does not by itself establish permanent alliance membership.                                                                                                                                                                                                                                                 |
| 朱府王爷绕境联盟         | Sites associated with the Zhu Fu Wang Ye procession, an ritual held annually on the 13th day of the first lunar month. According to the "Stele of Donations for Building the Divine Vessel" (《造僊鸼捐题碑》, 1851) , this ritual originated in 1849. However, it remains uncertain whether the tradition has continued uninterruptedly, or what changes have occurred regarding the identity of its participating alliance members. |
| 兴化分灵联盟           | Xinghua-related network of affiliated deity worship, including the Zhu Fu Wang Ye affiliation recorded at Poh Onn Kong.                                                                                                                                                                                                                                                                                                       |

A site may have several connections. These labels are research categories, not necessarily the official names of registered organisations. They should not be assumed to describe relationships that all existed at the same time.

### 3.3 Deities

Deity names are retained in Chinese to preserve the distinctions used in the source material and dataset. A recorded deity may be a principal deity, an additional deity, or a deity associated with an affiliated shrine. For example, the entry `朱府王爷（分灵）` at Poh Onn Kong describes affiliated worship and should not be read as identifying the temple's principal deity.
