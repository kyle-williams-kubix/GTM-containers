# Budget updates, performance review and next steps

Assigned too: Ky 
Client: Comodo Living
Created time: December 10, 2024 11:33 AM
Update Type: Routine Checks

Will be pulling back spend as results have tanked off the back of BFCM. We’ll continue to spend to maintain brand but at a slightly  reduced rate, as / when we see improvements in performance we can then look to increase budget. I suspect most users waited to purchase in the BFCM sale period. 

![Screenshot 2024-12-10 at 11.34.43.png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/Screenshot_2024-12-10_at_11.34.43.png)

Looking at the last 7 days, and comparing stats to the previous month, we have depleted the sales funnel and little users are in the mindset to purchase. Our way through this period is to continue pushing TOF and swatch purchase activity while we grow the sales funnel again. 

![Screenshot 2024-12-10 at 11.47.07.png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/Screenshot_2024-12-10_at_11.47.07.png)

This is what the current budget split looks like - 

![Screenshot 2024-12-10 at 11.57.57.png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/Screenshot_2024-12-10_at_11.57.57.png)

Looking into the traffic sources, most users are using IOS devices which leads us to think Elevar may not be the best platform considering safari is know to strip UTM parameters. 

![What platform are users using_.png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/What_platform_are_users_using_.png)

We are seeing this looking at traffic sources split by UTM source. 

![How does session performance vary by source_ (1).png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/c2498cf8-83f3-464f-a3bf-0e87ec4fd675.png)

We can further understand UTM tracking is off by looking at the revenue over time compared to attributed revenue from each platform.

We can fix this by using server side tagging via sGTM by masking UTM parameters when they are appended to a link in platform and apply an transformation before they are delivered to an reporting tool like GA4 or mixpanel. This will be crucial if we want to build cohort based on user interaction. 

![Revenue over time.png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/Revenue_over_time.png)

![Screenshot 2024-12-10 at 12.11.46.png](Budget%20updates,%20performance%20review%20and%20next%20steps%201587dee22b1780c1ba88d86b6963609d/2e91fe35-8365-4fff-ade4-bcfef926f0aa.png)