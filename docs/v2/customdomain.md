# Setting up a custom domain

## Prerequisites for this guide

- A domain (or subdomain) that you own
- 10-15 minutes of your time

## Setting up the domain

First, we need to access the DNS settings for your domain. This is usually done through your domain registrar. If you are unsure how to do this, please contact your domain registrar for assistance. In this example, our registar is [cloudflare](https://cloudflare.com) - however, the steps should be similar for other registrars.

Once you have accessed the DNS settings, you will need to add a `CNAME` record. This is usually done by clicking "Add Record" or "Add DNS Record" and selecting `CNAME` from the dropdown. In this example, we will be adding a `CNAME` record for `chub.transcribeit.live` to point to `custom.chub.page`.

![CNAME Record](https://img.sticks.ovh/dPxfRx-K-)

!!! warning "For Cloudflare Users"
    If you are using cloudflare, you will need to disable the orange cloud (proxy) for the `CNAME` record. This is done by clicking the orange cloud and setting it to grey. If you do not do this, you will not be able to use the custom domain and encounter an error.


After this is done, you will need to wait for the DNS to propagate. This can take anywhere from 5 minutes to 24 hours. Once this is done, you can continue to the next step.

## Checking the domain

To check if the domain is working, you can use a tool such as [whatsmydns.net](https://whatsmydns.net). Simply enter your domain and select `CNAME` from the dropdown. If you see a green checkmark, you are good to go. If you see a red X, you will need to wait for the DNS to propagate.

Then navigate to your domain in your browser. You should see your VTC's drivers hub. If you do not, please contact support.