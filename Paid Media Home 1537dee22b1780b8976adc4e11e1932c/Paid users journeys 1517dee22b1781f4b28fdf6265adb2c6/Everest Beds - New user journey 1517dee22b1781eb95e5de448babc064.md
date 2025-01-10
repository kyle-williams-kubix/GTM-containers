# Everest Beds - New user journey

Owner: Ky

Previous Journey

```mermaid
graph LR
    A[TOF PROSPECTING] 
    B[MOF PROSPECTING] 
    C[BOF PROSPECTING] 
    D[BOF RETARGETING]
	  G{Goal}
	  
	  
A
B--->D
C--->G
D--->G
```

New approach

- TOF Prospecting now optimises for content views targeting a range of audiences from lookalikes and detailed targeting.
- BOF is a dynamic shopping campaign retargeting users based on the products they have viewed or added to basket but not brought to then dynamically share recommendations
- BOF retargeting will then retarget users that have added to the cart within the past 90 days.
- We have a new MOF retargeting ad set designed to up sell users that have purchased an bed in the last 14 days.

```mermaid
graph LR
    A[TOF PROSPECTING] 
    B1[MOF RETARGETING - MATTRESSES] 
    B2[MOF RETARGETING - BEDS] 
    B3[MOF RETARGETING - MATTRESSES UP SELL] 
    C[BOF PROSPECTING] 
    D[BOF RETARGETING]
		
	  G{Goal}
	  
A --> B2
A --> B1

B1 --> D
B2 --> D
B3 ---> D

C --> G
D --> G

G --> B3

```

    ((Circle))
    (Round Rect)
    {Rhombus}