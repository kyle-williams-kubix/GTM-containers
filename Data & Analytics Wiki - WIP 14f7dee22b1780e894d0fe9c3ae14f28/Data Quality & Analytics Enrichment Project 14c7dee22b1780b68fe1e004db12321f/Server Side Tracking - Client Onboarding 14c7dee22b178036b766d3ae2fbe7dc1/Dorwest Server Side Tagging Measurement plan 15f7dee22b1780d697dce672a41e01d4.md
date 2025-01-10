# Dorwest Server Side Tagging | Measurement plan

Cost: £50.00
SST domain?: Yes
Who's paying: Client
Plan: PRO+
Status: Active
Tracking provider: Stape

# **Goals**

---

Migrate from traditional tracking methods to a server side solution where we aim to improve the quality of traffic being sent to marketing destinations, comply with privacy laws, and improve on accuracy. Thus improving the attributed results on platform giving a clearer picture of marketing activities. 

## Methodology

---

- **Setup**: Create an sGTM container in a cloud service and link it to the web GTM container.
- **Configure Tags**: Move and configure key tags (e.g., GA4, Meta Pixel) in sGTM.
- **Data Layer**:  Ensure clean and structured data flows from web GTM to sGTM.
- **Test**: Validate data flow, debug, and resolve errors.
- **Launch**: Deploy sGTM live, monitor performance, and optimise continuously.

We can make use of custom loaders, cookie keepers & no SQL databases to store user data and unique user_id. 

## MarTech tools

---

The tools used to setup server side tagging, the destination platforms as well as shopping feed apps. 

[Stape.io](http://Stape.io) - Server Side Tagging solution (Pro+ Plan)

[Mulwi](https://apps.shopify.com/omega-shopping-feeds?show_store_picker=1) - Product Feed app (Pro Plan)

GA4 - Website analytics

Google Ads - Pay per click advertising

Meta ads - Paid social advertising

Klaviyo - Email marketing tool

## UTM Plan

---

We’ll also be implementing a custom UTM strategy which will allow us track UTM’s more accurately in GA4 or any other tool which makes use of UTM parameters. 

To do this, the  parameters need to be changed. If UTM_source is used, this will continue to operate but keep in mind, you might lose visibility on some traffic. 

| Old | New  |
| --- | --- |
| utm_source | dw_sue |
| utm_medium | dw_mdm |
| utm_campaign | dw_cmn |

## Measurement Plan

---

GA4

[Events - Dorwest Measurement Plan](Dorwest%20Server%20Side%20Tagging%20Measurement%20plan%2015f7dee22b1780d697dce672a41e01d4/Events%20-%20Dorwest%20Measurement%20Plan%2015f7dee22b17809dae25eafe70e9bbc8.csv)

Meta

[Events - Dorwest Measurement Plan (1)](Dorwest%20Server%20Side%20Tagging%20Measurement%20plan%2015f7dee22b1780d697dce672a41e01d4/Events%20-%20Dorwest%20Measurement%20Plan%20(1)%201747dee22b1780ca8797eda30c5b4353.csv)

### Documentation

---

[User Properties - Dorwest Measurement Plan](Dorwest%20Server%20Side%20Tagging%20Measurement%20plan%2015f7dee22b1780d697dce672a41e01d4/User%20Properties%20-%20Dorwest%20Measurement%20Plan%2015f7dee22b1780beac5ec3be568dc2eb.csv)

[Event Parameters - Dorwest Measurement Plan](Dorwest%20Server%20Side%20Tagging%20Measurement%20plan%2015f7dee22b1780d697dce672a41e01d4/Event%20Parameters%20-%20Dorwest%20Measurement%20Plan%2015f7dee22b17803e93c9ee20bbc16994.csv)

[Testing documentation and sign off](Dorwest%20Server%20Side%20Tagging%20Measurement%20plan%2015f7dee22b1780d697dce672a41e01d4/Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be.md)