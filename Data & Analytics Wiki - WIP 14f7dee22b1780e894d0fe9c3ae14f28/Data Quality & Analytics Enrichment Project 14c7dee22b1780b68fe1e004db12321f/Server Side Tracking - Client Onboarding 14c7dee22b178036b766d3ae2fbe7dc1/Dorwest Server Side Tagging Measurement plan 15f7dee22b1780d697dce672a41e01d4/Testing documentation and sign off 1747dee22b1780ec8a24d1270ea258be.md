# Testing documentation and sign off

We migrated the clients current tracking process from simprosys to Stape. The platforms we migrated in this process include Google ads, GA4 and Meta with the scope to migrate Klaviyo in the future. 

Both GA4 and Google ads are using an anonymised data protocol to remove any personal identifies before sending any data to google. This allows us to maintain GDPR compliance, respect the users privacy and follow best practices for Google. Meta has been updated and will be transmitting only server side events. This is because we can pass more information along with the server side tags. 

The client has been informed that there may be fluctuations in performance while the platforms reconfigure themselves. The new Google ads goals have been set to secondary while the client informs their ads agency of the changes. 

Below is bit of a documentation of the final working product for reference. 

![WEB GTM sending data to GA4 via the server container url](Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be/Screenshot_2025-01-07_at_15.27.29.png)

WEB GTM sending data to GA4 via the server container url

![WEB GTM Data client sending events to the server container for all other tag types.](Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be/Screenshot_2025-01-07_at_15.27.40.png)

WEB GTM Data client sending events to the server container for all other tag types.

![Server side data meta tag sending events to meta](Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be/Screenshot_2025-01-07_at_15.26.10.png)

Server side data meta tag sending events to meta

![server side Google events, Left to right. Google ads, Google ads remarketing, conversion linker and GA4 tags](Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be/Screenshot_2025-01-07_at_15.29.18.png)

server side Google events, Left to right. Google ads, Google ads remarketing, conversion linker and GA4 tags

![Stape store - used for storing info to be recalled in future tags. Helps improve attribution, and identify users. ](Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be/Screenshot_2025-01-07_at_15.29.08.png)

Stape store - used for storing info to be recalled in future tags. Helps improve attribution, and identify users. 

![Server side meta events are being sent to as intended.](Testing%20documentation%20and%20sign%20off%201747dee22b1780ec8a24d1270ea258be/Screenshot_2025-01-07_at_16.13.13.png)

Server side meta events are being sent to as intended.