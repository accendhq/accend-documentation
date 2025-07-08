# NetSuite

To securely connect your NetSuite environment to Accend and enable automated syncing of financial data, please follow these steps to gather a few credentials from your NetSuite account.

Ensure you have **Administrator**-level access before proceeding.

### ✅ What You'll Need

To complete the connection, have the following items ready:

* **NetSuite Account ID**
* **Consumer Key**
* **Consumer Secret**
* **Token ID**
* **Token Secret**

***

### Step 1: Locate Your NetSuite Account ID

To find your Account ID:

1. Log into your NetSuite account.
2. Look at the web address in your browser—it will resemble this:\
   `https://7636429.app.netsuite.com/...`
3. The number before `.app.netsuite.com` is your Account ID.\
   In this example, it’s **7636429**.

You'll need to enter this Account ID into the **'Connect to NetSuite'** section during Accend’s connection setup process.

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.49.32 PM.png" alt=""><figcaption></figcaption></figure>

***

### Step 2: Enable Required SuiteCloud Features

In order for Accend to access your NetSuite data, you'll need to enable certain platform capabilities:

1. Navigate to [**Setup > Company > Enable Features**](http://system.netsuite.com/app/setup/features.nl?whence=).
2. Go to the **SuiteCloud** tab.
3. Enable these options by checking the boxes:
   * **SOAP Web Services**
   * **REST Web Services**
   * **Token-Based Authentication**
4. Click **Save** at the bottom of the page.

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.51.47 PM.png" alt=""><figcaption></figcaption></figure>

***

### Step 3: Install the Accend SuiteBundle

[**Click here to install Accend SuiteBudle**](https://system.netsuite.com/app/bundler/bundledetails.nl?sourcecompanyid=7636429\&domain=PRODUCTION\&config=F\&id=569515)

This SuiteBundle installs a predefined role and RESTlet scripts that grant Accend read-only access to your financial records.

* The bundle is typically provided by Accend Support or pre-linked via the onboarding flow.
* Follow the prompts in NetSuite to complete the installation.
* The installation may take a few minutes.

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.34.49 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.41.13 PM.png" alt=""><figcaption></figcaption></figure>

***

### Step 4: Assign a Role to a User

1. Go to [**Setup > Users/Roles > Manage Users**](https://system.netsuite.com/app/setup/listusers.nl?whence=).
2. Select an existing user account or create a new one.
   * To create a new user, go to **Lists > Employees > Employees > New**, then under the **Access** tab, check **Give Access**.
3. Edit the user’s profile. Under the **Access** tab, locate the **Roles** section.
4. Assign the role installed with the SuiteBundle: `Accend Financial Reports Role`.

> Tip: Many choose to assign the role to their own user to avoid using additional NetSuite seats.

***

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.55.59 PM (1).png" alt=""><figcaption></figcaption></figure>

### Step 5: Create an Integration Record

To obtain your **Consumer Key** and **Consumer Secret**, follow these steps:

1. Go to [**Setup > Integrations > Manage Integrations > New**](https://system.netsuite.com/app/common/integration/integrapp.nl?whence=).
2. Fill out the form with:
   * **Name**: Choose any descriptive name (e.g., “Accend Integration”)
3. Check the following options:
   * **Token-Based Authentication**
4. Save the integration.
5. Once saved, NetSuite will show your **Consumer Key** and **Consumer Secret**.

{% hint style="danger" %}
<mark style="color:red;">**Important:**</mark> <mark style="color:red;"></mark><mark style="color:red;">Copy and securely store your Consumer Key and Consumer Secret immediately after saving—they will not be displayed again.</mark>
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.57.36 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 3.57.52 PM (1).png" alt=""><figcaption><p>Copy <strong>Consumer Key</strong> and <strong>Consumer Secret</strong></p></figcaption></figure>

***

### Step 6: Generate Access Token

1. Navigate to [**Setup > Users/Roles > Access Tokens > New**](https://system.netsuite.com/app/setup/accesstoken.nl?whence=).
2. Select:
   * The integration you just created.
   * The user assigned in Step 4.
   * The role added via the SuiteBundle (Accend Financial Reports Role).
3. Click **Save** to generate the credentials.
4. NetSuite will show your **Token ID** and **Token Secret**.

{% hint style="danger" %}
<mark style="color:red;">**Important:**</mark> <mark style="color:red;"></mark><mark style="color:red;">Copy and securely store your Token ID and Token Secret immediately—they cannot be retrieved later.</mark>
{% endhint %}

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 4.00.32 PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2025-06-24 at 4.00.49 PM.png" alt=""><figcaption><p>Copy <strong>Token ID</strong> and <strong>Token Secret</strong></p></figcaption></figure>

***

### Step 7: Enter Credentials in Accend

When prompted in the Accend setup interface, provide:

* **Account ID** – From Step 1
* **Consumer Key** – From Step 5
* **Consumer Secret** – From Step 5
* **Token ID** – From Step 6
* **Token Secret** – From Step 6

Once all credentials are entered correctly, the connection should be established, and Accend will be able to sync your NetSuite financial data securely.

**Security Assurance:** Accend uses these credentials only to securely access and sync your NetSuite data. Your credentials are encrypted and stored securely.



