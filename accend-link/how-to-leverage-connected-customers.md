---
icon: wave-square
---

# How to leverage connected customers

### Data Sync

1. **Initial Sync**
   1. Triggered when a customer first connects their accounting software to Accend.
   2. During this process, Accend pulls and stores up to **36 months** of historical financial data available from the integration.
2. **Recurring Sync**
   1. Runs automatically on a monthly schedule after the initial sync is complete.
   2. This process updates the most recent month’s financial data to ensure that the system remains up to date.

#### Webhook event

Accend provides webhook notifications so your application can react to data sync events in real time. There are two types of webhook events:

1. [Sync Completion event](https://app.gitbook.com/o/c6StG9bTL85tJU742xqN/s/C1dyFADp05ltoHZNkN2k/~/changes/31/engineering/openapi/financials#link_sync_completion_event)
   1. Sent when a data sync (initial or recurring) has successfully finished.
   2. The payload includes information about the sync type (`initial` or `recurring`) and the customer it pertains to and the data period we retrieved.
2. [Sync Error event](https://accend.gitbook.io/accend-docs/engineering/openapi/financials#link_sync_error_event)
   1. Sent if a data sync fails due to an error.
   2. The payload includes details about the error and the affected customer, which can be used for debugging or retry logic.



* If you are creating financial spreading cases as part of customer onboarding, you should do so **after** receiving a `Sync Completion` webhook for a sync of type `initial`.\
  At that point, all required historical data will be available, and you can create a spreading case with the appropriate spreading periods.
* If you are performing periodic financial reviews, you can use the `GET /api/v1/financials/customers` endpoint (described below) to retrieve connected customers, and then create a spreading case with the specific spreading periods you require.

### Managing Connected Customers

You can query connected customers and manage their accounting integrations using the Customers API and related endpoints:

*   **Retrieve Connected Customers**\
    Use the [`GET /api/v1/financials/customers`](https://accend.gitbook.io/accend-docs/engineering/openapi/financials#get-api-v1-financials-customers) endpoint with the filter:

    ```json
    contains_any("link_connections", "all")
    ```

    This returns all customers with at least one active accounting software connection.
* **Manage Connections**\
  Once you’ve identified connected customers, you can use the **Link APIs** to:
  * Retrieve detailed information about a specific connection  `/api/v1/financials/link/customers/{customer_id}/link_connections`
  * Disconnect an existing connection  `/api/v1/financials/link/customers/{customer_id}/link_connections/{link_connection_id}/disconnect`
  * Make pass-through API calls to the underlying accounting platform  `/api/v1/financials/link/customers/{customer_id}/link_connections/{link_connection_id}/pass_through`
