# Data - Situational Analysis

Assigned too: Ky 
Client: Ted Baker
Created time: December 10, 2024 9:49 AM
Update Type: Data Quality

Elevar is reporting 101% data accuracy for some platforms:

US ad account is showing 55% data accuracy. 

Channel summary for the last 24 hours shows inconsistencies with meta over reporting. 

![Screenshot 2024-12-10 at 09.51.25.png](Data%20-%20Situational%20Analysis%201587dee22b17808090a1d8acc7f065ff/Screenshot_2024-12-10_at_09.51.25.png)

We still are waiting for elevar to complete the setup. They have confirmed they **cannot** split info by markets as well as have one rollup property. 

Elevar support confirmed its not technically possible and they only provide a workaround. My concern (@Ky ) with this is continued support and ongoing updates and changes on their end may destroy this setup which would be a concern. 

![Screenshot 2024-12-11 at 08.58.21.png](Data%20-%20Situational%20Analysis%201587dee22b17808090a1d8acc7f065ff/Screenshot_2024-12-11_at_08.58.21.png)

Currently exploring Funnel as a reporting tool for Ted Baker. Goal is pushing data into a spreadsheet as a way to track data. 

We can use Funnel as a ETL tool to extract data from platforms, apply transformations so it’s unified for reporting and load it into a destination. 

```mermaid
architecture-beta
    group etl(cloud)[ETL Process]

    service silo(database)[Data Silo] in etl
    service funnel(server)[Funnel] in etl
    service destination(cloud)[Destination] in etl

    silo:R --> L:funnel
    funnel:R --> L:destination

```

Tech stack would looks like:

Our data silos will feed data into [Funnel.io](http://Funnel.io), acting as our warehouse and single point for reporting. 

Any filtering and transformations (i.e currency, funnel stage, combined metrics, formulas) will be handled within funnel. 

Once Transformed, the data is free to flow into any destination we desire. 

```mermaid
graph TD
  
  S1[(Silo 1)]
  S2[(Silo 2)]
  S3[(Silo 3)]
  S4[(Silo 4)]
  S5[(Silo 5)]

	T1[funnel.io]
	
	T1.1[/Data Transformations\]
	
	L1{{Destination 1}}
	L2{{Destination 2}}
	L3{{Destination 3}}
	
	S1 & S2 & S3 & S4 & S5 --> T1
	
	T1 --> T1.1
	T1.1 --> L1 & L2 & L3
```

```mermaid
graph TD
  
  S1[(Meta Ads)]
  S2[(Google Ads)]
  S3[(Snapchat Ads)]
  S4[(Pintrest Ads)]
  S5[(TikTok Ads)]

	T1[funnel.io]
	
	T1.1[/Data Transformations\]
	
	L1{{Google Sheets}}
	
	S1 & S2 & S3 & S4 & S5 --> T1
	
	T1 --> T1.1
	T1.1 --> L1
```