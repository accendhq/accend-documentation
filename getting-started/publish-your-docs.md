---
icon: rectangle-code
---

# Engineering Quickstart

### Accend Financial Spreading Product Usage Options

Accend offers flexible integration options to match your company’s needs and engineering resources, allowing for varying levels of integration.

#### Dashboard Only

The quickest way to start leveraging Accend for financial spreading.

* Create and review financial spreading cases directly in the Accend dashboard.
* Download case results in Excel format for underwriting analysis or CSV format for DB import.

#### Dashboard + JSON Data Processing

Expand functionality for programmatic analysis.

* Create and review financial spreading cases in the Accend dashboard.
* Download case results in JSON format and feed into your systems for programmatic analysis.

#### Dashboard + Automated Webhook Integration

Enhance automation by setting up a webhook to receive case results directly.

* Create financial spreading cases in the Accend dashboard.
* [Configure a webhook server to automatically receive case results](https://api.staging.withaccend.com/redoc#tag/Financials/operation/financial_statement_case_process_completion_eventfinancial_statement_cases_event_post) as soon as they’re available.
* You can set up the webhook URL and test it in Accend dashboard settings as an admin user.

#### Full Automation via API Integration

Achieve end-to-end automation with Accend’s API integration for programmatic creation of spreading cases and result processing.

* Recommended workflow (testing and development recommended on our staging environment):
*
  1. [Create a customer profile](https://api.staging.withaccend.com/redoc#tag/Financials/operation/create_customer_api_v1_financials_customers_post) if they are new to the Accend system.
  2. [Upload customer documents](https://api.staging.withaccend.com/redoc#tag/Financials/operation/update_customer_api_v1_financials_customers_put).
  3. [Initiate a financial spreading case.](https://api.staging.withaccend.com/redoc#tag/Financials/operation/create_fin_stmt_spreading_case_api_v1_financials_cases_post)

[Receive case results via webhook](https://api.staging.withaccend.com/redoc#tag/Financials/operation/financial_statement_case_process_completion_eventfinancial_statement_cases_event_post) for complete process automation.
