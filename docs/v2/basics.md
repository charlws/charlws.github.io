## Prerequisites for this guide
- As outlined in the [getting started](landing.md) guide
- 10-15 minutes of your time

## Basic Setup

Welcome to basic setup. This will help you get to a point where you can start using the drivers hub. Let's follow the steps below to get started.

### Creating a VTC

Go to the [Creation](https://drivershub.charlws.com/setup) page

![Creation Page](https://img.sticks.ovh/TvYB1ljxO)

Choose any plugins you'd like. 

![Plugins](https://img.sticks.ovh/i2ugZbtR5)

!!! note "About Plugins..."
    Some are included (as demoted by the free next to the name), however some require a one time payment to use. If you do end up choosing a paid plugin, you **need to send payment ASAP** or your VTC will be **disabled** until payment is received.

    The payment address (paypal) is: `billing@charlws.com`

Choose the subscription you'd like.

![Subscriptions](https://img.sticks.ovh/W6byuluWr)

Fill out the form with your VTC information (as shown below)

![Form](https://img.sticks.ovh/CjCx-pg8H)

!!! warning "Domains/Domain Endings"
    If you are using a custom domain, you **must** have a **cname** pointing to `custom.chub.page`. If you do not, you will not be able to use the custom domain. SSL Will be 
    automatically generated for you. If you need more assistance, please see the [custom domain](custom-domain-setup) page for more detailed steps.

    If you are using a custom domain, set the "drives hub domain" to the domain you are using. If you are not using a custom domain and using the subdomain of CHub, the format is `yourvtc.chub.page`

    Failure to do so will result in the following error:
    
    ![Bad Domain Error](https://img.sticks.ovh/-YvoXUn2G)
!!! note "How to obtain steam ID/API Key"
    It's really easy to get your steam ID and API key. Just follow the steps below:
    
    1. Go to [steamid.pro](https://steamid.pro/)
    2. Enter your steam profile URL (find it by going to your steam profile and copying the URL)
    3. Click submit and copy the `SteamID` value and paste it into "Your Steam ID" on the form
    4. Go to [steamcommunity.com/dev/apikey](https://steamcommunity.com/dev/apikey) and click "Create a new key" (or copy your existing key)
    5. Copy the key and paste it into "Your Steam API Key" on the form (in the above example, it's blurred out for security reasons)

Then click submit. 

## After Creation

After you've created your VTC, you will see two things occur:

- A little message will appear below the button with your VTC information. Be sure to save this information somewhere safe as you will need it later.

![Message](https://img.sticks.ovh/ywUb5qbH8)

!!! warning
    Please be sure to write down the information shown in the message including the admin password. **THE ADMIN PASSWORD WILL NOT BE SHOWN AGAIN**. If you lose it, you will need to contact support to reset it.

- A message about billing will also be sent to you from the CHub

![Billing](https://img.sticks.ovh/MwwKa9L1G)

If everything looks correct, you can now go to your VTC page. You can do this by clicking the vtc link. If you are using a custom domain, you can go to that domain instead.

Now proceed to the [next section](config) to continue setting up your VTC.