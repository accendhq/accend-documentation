# Setup

**Setting Up a Zoho Books App**

**Create Zoho Accounts**

* Sign up for [a Zoho Books account](https://www.zoho.com/us/books/).
* Then, create [a Zoho Developer account](https://api-console.zoho.com/).

**Register a New App**\
In the [Zoho Books API Console](https://api-console.zoho.com/), create a new app to generate your OAuth credentials.

**Configure Redirect URI for Accend**\
In your app settings under **Authorized Redirect URIs**, add the following Accend redirect URI:

```
https://connections.withaccend.com/link/connect/zoho_books
```

**Share OAuth Credentials with Accend**

* Locate your **Client ID** and **Client Secret** under your application in the API Console.
* Enter these credentials into the **Integration** section of your Accend Dashboard to complete the setup.
