# Setup

#### **Setting Up a QuickBooks Online App**

**Create an Intuit Developer Account**\
Sign up at the [Intuit Developer Portal](https://developer.intuit.com/) to get started.

**Register a New App**\
Within the Developer Portal, create a new app to generate your OAuth credentials.

**Setup Permissions**

In your app settings under **Permissions**, select `com.intuit.quickbooks.accounting` .

**Configure Redirect URI for Accend**\
In your app settings under **Redirect URIs**, add the Accend redirect URI:

<pre><code><strong>https://connections.withaccend.com/link/connect/quickbooks_online
</strong></code></pre>

**Share OAuth Credentials with Accend**\
Locate your **Client ID** and **Client Secret** in the Developer Portal.\
Enter these credentials into the **Integration** section of your Accend Dashboard to complete the setup.

<figure><img src="../../../.gitbook/assets/Screenshot 2025-05-14 at 4.15.08 PM.png" alt=""><figcaption></figcaption></figure>

**Move to Production**\
To transition from sandbox to production:

* Fill out the App Assessment Questionnaire provided by Intuit.
* Provide complete and accurate information about your app.
* Submit the questionnaire for review.

Once approved, Intuit will issue production credentials, allowing full access to live QuickBooks Online data.

