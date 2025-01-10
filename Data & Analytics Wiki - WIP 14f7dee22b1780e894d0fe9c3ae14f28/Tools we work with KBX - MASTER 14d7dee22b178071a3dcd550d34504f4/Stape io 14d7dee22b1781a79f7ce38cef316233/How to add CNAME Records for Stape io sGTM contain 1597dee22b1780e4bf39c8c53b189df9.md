# How to add CNAME Records for Stape.io sGTM containers

<aside>
💡

This is key to make use of any cookie extenders, and further enhance the ability to prevent ad blockers and tracking preventions from stopping tracking tags.

</aside>

To add CNAME records, follow these general steps. 

The specifics may vary slightly depending on your domain registrar or hosting provider:

1. **Log in to your Domain Registrar or DNS Provider**: Access the dashboard where you manage your domain (e.g., GoDaddy, Namecheap, Cloudflare, etc.).

1. **Go to DNS Management**: Look for options like "DNS Management," "DNS Settings," or similar.

1. **Add the First CNAME Record**:
    - **Record Type**: Select **CNAME**.
    - **Host/Name**: Enter `sst`
    - **Value/Target**: Enter `eup.stape.net`
    - **TTL (Time to Live)**: Set to default or a low value like **3600 seconds / 1 hour** if you have this option.
    
2. **Add the Second CNAME Record**:
    - **Record Type**: Select **CNAME**.
    - **Host/Name**: Enter `load.sst`
    - **Value/Target**: Enter `leup.stape.net`
    - **TTL**: Again, set to default or **3600 seconds / 1 hour**.
    

**Save/Apply Changes**: Confirm and save each record. DNS changes might take a few minutes to a few hours to propagate fully, so allow some time for the records to become active.

Please inform the Account Manager when this has been completed.