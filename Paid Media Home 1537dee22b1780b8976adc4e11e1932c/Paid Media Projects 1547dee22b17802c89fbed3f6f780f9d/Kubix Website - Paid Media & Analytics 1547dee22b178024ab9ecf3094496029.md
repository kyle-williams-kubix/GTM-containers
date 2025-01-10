# Kubix Website - Paid Media & Analytics

# Situational analysis:

1. Currently the website is using basic integrations and auto tagging for GA4 and Google ads.
2. The site has two google tags, it doesn't look like we are subject to double counting but data loss could be an issue and we’re not following best practice.
3. User provided data is not being passed with tags making it impossible to identify users when they submit a form submission. This needs to be looked into as to the reason why these parameters are not being passed into the `datalayer` so they can be picked up.

## Tasks to complete:

### Server side tagging:

Address the issue with forms not passing user provided data, this could be as simple as a `window.datalayer` push based on the forms fields (as long as webflow allows you to interact with `dom` elements). 

### Server side tagging:

Setup and implement stape, we can get started on the free plan but i’d like us to be on the pro plan to make use of stape store to identify new and returning prospects. 

### Advanced Analytics:

Setup and implement [Mix panel](https://www.notion.so/Mixpanel-14d7dee22b1781be9092d3b797128d94?pvs=21) instead of GA4 for detailed analysis on performance and understanding what is driving MQL’s. This can help provide an detailed activity log within hub spot for prospecting and converting leads. it opens up the door to dynamically remarking people based on actions and opens the door to marketing automations. 

### Consent mode Platform

Default consent status is set in the custom code section of the webflow site:

```jsx

<script>
       window.dataLayer = window.dataLayer || [];
       function gtag(){dataLayer.push(arguments);}
       
       if(localStorage.getItem('consentMode') === null){
           gtag('consent', 'default', {
               	'ad_storage': 'denied', //Google Ads
               	'analytics_storage': 'denied', //Google Analytics
               	'personalization_storage': 'denied', //e.g reccomendations based on previous browsing
                'ad_user_data': 'denied', // Ad user data storage (e.g., storing user data for ad targeting).
                'ad_personalization': 'denied', // Ad personalization (e.g., tailoring ads based on user preferences and behaviour).
               	'functionality_storage': 'denied', //Functionality e.g Language selected
              	'security_storage': 'denied', //Auth and Authentication
           });
       } else {
           gtag('consent', 'default', JSON.parse(localStorage.getItem('consentMode')));
       }
</script>
```

This isn't technically working properly though since by default, consent is denied but there is no way for a user to give permission to be tracked. we are seeing events in GA4 though indicating users are being tracked without the appropriate GDPR measures in place. 

We can get rid of this custom js code and use something like CookieYes to handle consent mode: https://www.cookieyes.com/

The **basic** plan is ideal so we can use custom CSS to handle the look and layout of the consent banner. 

# Measurement Plan

[Kubixmedia.co.uk](https://www.notion.so/Kubixmedia-co-uk-1547dee22b17803ab75be467c17f3c18?pvs=21)