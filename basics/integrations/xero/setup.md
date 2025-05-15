# Setup

#### **Setting Up a Xero App**

**Create a Xero Developer Account**\
[Start by creating a Xero account](https://www.xero.com/us/signup/developers/), then activate your developer access via the Xero Developer Portal.

**Register a New App**\
Within the [Developer Portal](https://developer.xero.com/), create a new app to obtain your OAuth credentials.

* **Integration type:** Select **Web app**
*   **Redirect URI:** Add the Accend redirect URI:

    ```
    https://connections.withaccend.com/link/connect/xero
    ```

**Share OAuth Credentials with Accend**\
Find your **Client ID** and **Client Secret** in the Developer Portal -> App -> Configuration.\
Enter these credentials into the **Integration** section of your Accend Dashboard to complete the setup.



**NOTE: Xero App Partner Program**\
By default, Xero apps are limited to 25 connected organizations. To support more customers, you must apply to [become a Xero App Partner](https://developer.xero.com/documentation/xero-app-store/app-partner-guides/become-an-app-partner/). Approval lifts the connection limit and grants access to additional features and support.
