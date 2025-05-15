# Setup

**Setting Up a FreshBooks App**

**Create a FreshBooks Account**\
Start by signing up for a [FreshBooks account](https://www.freshbooks.com/).

**Register a New App**\
In [the FreshBooks Developer Portal](https://my.freshbooks.com/#/developer), create a new app to generate your OAuth credentials.\
When configuring your app, request the following scopes:

* `user:profile:read`
* `user:account:read`
* `user:journal_entries:read`
* `user:reports:read`

**Configure Redirect URI for Accend**\
In your app settings under **Redirect URIs**, add the following Accend redirect URI:

```
https://connections.withaccend.com/link/connect/freshbooks
```

**Share OAuth Credentials with Accend**\
Locate your **Client ID** and **Client Secret** in the Developer Portal for your App.\
Enter these credentials into the **Integration** section of your Accend Dashboard to complete the setup.

***
