## Prerequisites for this guide
- Followed the [basic setup](/docs/v2/basics) guide
- 20-30 minutes of your time

## Basic Configuration
### Getting the basics setup
Now that you've created your VTC, you will need to configure it. To do this, go to the domain you chose for your VTC. You will be greeted with a page that looks like this:

![Welcome](https://img.sticks.ovh/APfBVTc8M)

Login with the credentials you created when you created your VTC. You will be greeted with a page that looks like this:

![Dashboard](https://img.sticks.ovh/wfC2CRN_Q)

Scroll down until you see the "Configuration" section - click it and then click the "Web" tab. You will be greeted with a page that looks like this:

![Web Config](https://img.sticks.ovh/NXpCTOMsN)

Fill out the form, note that Custom Application and Custom Style is not required. 

![Web Config Filled](https://img.sticks.ovh/NXpCTOMsN)

!!! note "Form Meanings"
    Name, Distance Unit, Slogan, are self explanatory.
    
    Navio / TruckSim Company ID is the ID of your company on the respective platform. If you don't have a company on one of the platforms, you can leave it blank. This will be 
    covered in more detail later in this guide.
    
    Color is the accent color for your VTC. This is used in buttons and other places. 
    
    Logo Download link is the link to your logo. If you don't have a logo, you can leave this blank.
    
    Banner download link is for the banner on your VTC page. If you don't have a banner, you can leave this blank.
    
    Custom Application and Custom Styles are advanced features and are not required. If you don't know what these are, you can leave them blank.

Click save to apply your changes.

At this point, you do have a working VTC. However, **we still recommend you continue with the rest of this guide** to get the most out of your VTC with CHub - some features will not work without the rest of this guide.

## JSON Configuration (Advanced)

!!! warning "JSON Configuration is an advanced feature."
    This section allows you to configure your VTC in more detail. Please note that values and formatting are **sensitive**. If you are unsure of what you are doing, please ask in the support channel on discord. We are always happy to help.

### Getting Started
On the configuration page, click the "API (JSON)" tab. You will be greeted with a page that looks like this:

![JSON Config](https://img.sticks.ovh/_-ClUhNSJ)

We will be going through each section of this page in detail. But first, a quick overview of how to use JSON and what it is.

### What is JSON?
JSON is a data format that is used to store data in a human readable format. It is used by many applications and is very common. It is also used by CHub to store VTC information,
such as the VTC name, slogan, etc. 

Here's an example of what JSON looks like:

```json
{
  "foo": "bar",
  "this": "is",
  "an": "example"
}
```

As you can see, it's very easy to read and understand. It's also very easy to write. Let's break down the above example.

1. The first line is the opening of the JSON object (`{`) - this is required for all JSON objects.
2. The first key appears on the second line (`foo`) - this is the name of the value. This is also required for all JSON objects. All keys are surrounded by quotes (`"`) - this is also required.
2. The seperator between the first key and value is a colon (`:`) - this is required for all JSON objects.
3. The first value (after `:`) is `bar` - this is the name of the value. This is also required for all JSON objects. All values are surrounded by quotes (`"`) - this is also required.
4. After the end of the value, there is a comma (`,`) - this is required for all JSON objects except the last one. This is used to separate the key/value pairs.
5. This process repeats until the last key/value pair.

!!! note "JSON Objects, Keys, Values and pairs"
    JSON objects are surrounded by curly braces (`{}`) - this is required for all JSON objects.
    
    JSON keys are surrounded by quotes (`"`) - this is required for all JSON keys.
    
    JSON values are surrounded by quotes (`"`) - this is required for all JSON values.
    
    JSON key/value pairs are separated by commas (`,`) - this is required for all JSON key/value pairs except the last one.

    JSON Pairs also seprate on the line, using `:` - this is required for all JSON key/value pairs.


### Other Information
Here is some other information about JSON that you should know.

#### JSON Arrays

JSON Also includes arrays, which are used to store lists of data. Here's an example of what a JSON array looks like:

```json
[
  "foo",
  "bar",
  "baz"
]
```

As you can see, it's very easy to read and understand. It's also very easy to write. Another example:

```json
[
  {
    "foo": "bar"
  },
  {
    "bar": "baz"
  }
]
```

The rest of the guide will teach you how to use arrays, but this is just a quick overview of what they are.

#### Common JSON Errors

JSON is very sensitive to formatting. If you make a mistake, it will not work. Here are some common errors:

1. Missing a comma (`,`) - this is required for all JSON key/value pairs except the last one.
2. Missing a quote (`"`) - this is required for all JSON keys and values.
3. Missing a colon (`:`) - this is required for all JSON key/value pairs.
4. Missing a curly brace (`{}`) - this is required for all JSON objects.
5. Missing a square bracket (`[]`) - this is required for all JSON arrays.

If you make a mistake, you can use the revert button to revert your changes. If you need to start over, you can use the "Reset" button at the bottom of the page. **Remember to save your changes and reload the config/server after making changes!**

#### Common JSON Lingo
`bool/boolean` - A boolean value is a value that is either `true` or `false`. This is used in JSON to represent a boolean value.

`int/integer` - An integer value is a value that is a number. This is used in JSON to represent a number.

`string` - A string value is a value that is a string. This is used in JSON to represent a string. All strings are surrounded by quotes (`"`).

`enum` - An enum value is a value that is a string. This is used in JSON to represent a string. All strings are surrounded by quotes (`"`). The value must be one of the values listed in the documentation. If you use a value that is not listed in the documentation, it will not work.

Great! Now that we know what JSON is and how to use it, let's get started with the configuration.

## Configuration (JSON)

!!! warning "Please change values with care!"
    Please note that some values are **sensitive** and changing them may break your VTC. The revert button can help you, or if you need to start over, you can use the "Reset" button at the bottom of the page. **Remember to save your changes and reload the config/server after making changes!**

We will be going line-by line through the JSON configuration. Please note that some values are required and some are not. If a value is required, it will be marked as such.

### Name
`name` is the name of your VTC. This is displayed on the VTC page and in the application. This is a required field.

### Language
!!! note "Language codes"
    Language codes are two letter codes that represent a language. For example, English is `en`, French is `fr`, etc. You can find a list of language codes [here](https://www.andiamo.co.uk/resources/iso-language-codes/).

`language` is the two letter language code of your VTC. This is displayed on the VTC page and in the application. This is a required field.

### Distance Unit
!!! note "Possible Values"
    Possible values are `metric` or `imperial`.

`distance_unit` is the unit of distance your VTC uses. By default, most of the CHub application uses **km**, however if this is set to `imperial`, it will **convert** to **miles**. This is a required field.

### Privacy
`privacy` (TBD)

### Security Level
`security_level` (TBD)

### Hex Color
`hex_color` is the hex color of your VTC. This is used in buttons and other places. This is a required field.

Example: 

![Hex Color](https://img.sticks.ovh/24S3_drCh)

!!! note
    In this example, the hex color is `#0000FF` - this is the value you would put in the JSON configuration. 


### Logo URL
`logo_url` is the URL to your VTC logo. This is displayed on the VTC page. This is a required field.


### Guild ID
!!! note "Conditional Require/Information"
    This is only required if you plan to use discord features of CHub. If you don't know how to get your guild ID, please see [this](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) article on how to get your guild ID.

`guild_id` is the ID of your discord server. This is used to link your discord server to your VTC.

### Must Join Guild? 
!!! note "Possible Values"
    Possible values are `true` or `false`.

`must_join_guild` is a boolean value that determines if users must join your discord server to use your VTC. 


### Use Server Nickname?

!!! note "Possible Values"
    Possible values are `true` or `false`.

`use_server_nickname` is a boolean value that determines if CHub should use the user's discord nickname or their username set inside of CHub.

### Allow Custom Profile?

!!! note "Possible Values"
    Possible values are `true` or `false`.

`allow_custom_profile` is a boolean value that determines if users can set a custom profile. If this is set to `false`, users will not be able to set a custom profile.


### Avatar Domain Whitelist
`avatar_domain_whitelist` is a list of domains that users can use for their avatar. If a user tries to use an avatar from a domain that is not in this list, it will be rejected. This is a required field.

Example:

```json
[
  "https://cdn.discordapp.com",
  "https://cdn.discord.com"
]
```

!!! warning
    If this list is empty, users will not be able to set an avatar. Please make sure this has a good amount of common URLs in it to allow freedom for users to set their avatar.

### Required Connections
!!! note "Possible ENUM Values"
    Possible values are `discord`, `truckersmp`, and `email`

`required_connections` is a list of connections that users must have to use your VTC. If a user does not have one of these connections, they will need to link or their account will 
be limited. This is a required field.

Example:

```json
[
  "discord",
  "truckersmp"
]
```

In this example, users will need to have discord and truckersmp linked to use the VTC. Please be sure to use only the values listed above. If you use a value that is not listed above, it will not work.

### Register Methods
!!! note "Possible ENUM Values"
    Possible values are `discord`, `steam`, and `email`

This is almost the same as `required_connections`, however this is used for the registration page. This is a required field.

Example:

```json
[
  "discord",
  "steam"
]
```

In this example, users will be able to register with discord and steam. Please be sure to use only the values listed above. If you use a value that is not listed above, it will not work.

### Tracker
!!! warning "Only one option currently available"
    Due to navio shutting down, this should always be `tracksim`

`tracker` is the tracker that your VTC uses. This is used to track jobs and mileage. This is a required field.

### Tracker Company ID

!!! note "Conditional Require/Information"
    This is only required if you plan to use the tracker features of CHub. If you don't know how to get your company ID, please see [this](https://docs.tracksim.app/docs/company-id) article on how to get your company ID.

`tracker_company_id` is the ID of your company on the tracker. This is a required field.

### Tracker API Key

!!! note "Conditional Require/Information"
    This is only required if you plan to use the tracker features of CHub. If you don't know how to get your API key, please see [this](https://docs.tracksim.app/docs/api/authentication) article on how to get your API key.

`tracker_api_key` is the API key of your company on the tracker. This is a required field.

### Tracker Webhook Secret
`tracker_webhook_secret` (TBD)

### Delivery Rules
`delivery_rules` (TBD)

### Delivery Log Channel ID
!!! note "Conditional Require/Information"
    This is only required if you plan to use the tracker features of CHub. If you don't know how to get your channel ID, please see [this](https://support.discord.com/hc/en-us/articles/206346498-Where-can-I-find-my-User-Server-Message-ID-) article on how to get your channel ID.

`delivery_log_channel_id` is the ID of the channel you want to log deliveries to. 

### Delivery post gifs
!!! note "Conditional Require"
    This is only required if you plan to use the tracker features of CHub.

`delivery_post_gifs` is a list of gifs to post in the embed along with the delivery. This is a required field. We already include some gifs for you, but you can add more if you'd like. Most people will not need to change this.

Example:

```json
[
  "https://c.tenor.com/fjTTED8MZxIAAAAC/truck.gif",
  "https://c.tenor.com/QhMgCV8uMvIAAAAC/airtime-weeee.gif",
]
```

### Discord Settings
!!! warning "This module must be followed in it's entirety to work properly."
    This section is for discord settings. This is required if you plan to use discord features of CHub. If you do not plan to use discord features of CHub, you can skip this section.

`discord_client_id`, `discord_client_secret`, `discord_bot_token` are all used for discord integration. These are required fields.

#### Creating the Discord App/Bot
First, Go to [discord.com/developers](https://discord.com/developers) and login with your discord account.

!!! note "Team Recommended"
    We recommend creating a team for your VTC. This will allow you to add other members of your VTC to the discord app. This is not required, but recommended for 
    higher ranks to edit the bot/applications.

#### Creating the team (optional)
If creating a team, click "Teams", and the new button. You'll see a popup like this:

![New Team Creation](https://img.sticks.ovh/MdMscu6iU)

Fill out the form and click "Create Team". You'll be greeted with a page that looks like this:
![Team Dash](https://img.sticks.ovh/zFuMs6Ojr)

Be sure to add people to the team, aswell as add a logo to it.


#### Creating the application
Go back to the [applications page](https://discord.com/developers/applications) and click "New Application". You'll see a popup like this:

![New App Creation](https://img.sticks.ovh/u9ryfFo3O)

Fill out the form and click "Create". If using a team, make sure to select it from the dropdown. You'll be greeted with a page that looks like this after creation:

![App Dash](https://img.sticks.ovh/6hB4lAiVL)

Fill out the Description field to something that makes sense to you. Save, and click the "Bot" tab. You'll be greeted with a page that looks like this:

![Bot Dash](https://img.sticks.ovh/w7wDMIOVl)

On this page, you need to do the following:

1. Click "Reset Token" and confirm the popup. This will generate a new token for your bot. **You will need this later.**
2. Make sure all intents are enabled 
3. Make sure the bot is public

#### Linking the bot to CHub
Now with the bot created, we need to link it to CHub. Click on the OAuth2 tab. You'll be greeted with a page that looks like this:

![OAuth2 Dash](https://img.sticks.ovh/rDZ9Lq-WM)

On this page, you need to do the following:

1. Copy the Client ID and paste it into the `discord_client_id` field in the JSON configuration.
2. Click "Reset Secret" and confirm the popup. Then paste the secret into the `discord_client_secret` field in the JSON configuration.
3. Paste the bot token into the `discord_bot_token` field in the JSON configuration.

After that, you can close the discord developer portal and save the JSON configuration, reload, and then click "Activate Discord Role Connection" on the configuration page. You should see a popup like this:

(TBD)

#### Adding the bot to your server
Now that the bot is linked to CHub, we need to add it to your server. To do this, go back to the [applications page](https://discord.com/developers/applications) and click on your application. Click the "OAuth2" tab and you'll be greeted with a page that looks like this:

![OAuth2 Dash](https://img.sticks.ovh/rDZ9Lq-WM)

Click the "URL Generator" page, and select the following below:

![URL Generator](https://img.sticks.ovh/3h4mGPktD)

Scroll down, click "Copy" and paste the URL into your browser. Choose your server and click "Authorize" - the bot should now be in your server.

### Custom SMTP/Email Settings
!!! warning
    This is a fairly advanced feature. Most VTCs can leave this blank.

`smtp_host`, `smtp_port`, `smtp_email`, `smtp_password`, `smtp_passwd`, are all used for SMTP integration. These are required fields if you plan to use SMTP integration.

Set these values to the values of your SMTP server. If you don't know what these are, please contact your email provider.

#### Email Templates
`email_template` is a list of email templates that are used for sending emails. This is a required field.

The three templates are:

- `register`

- `update_email`

- `reset_password`

Each template has a `subject`, `from_email`, `html` and `plain` field. These are all required fields.

`subject` is the subject of the email. This is a required field.

`from_email` is the email address the email is from. This is a required field.

`html` is the HTML version of the email. This is a required field.

`plain` is the plain text version of the email. This is a required field.