# Table of contents

* [Welcome](README.md)

## Getting Started

* [Dashboard Quickstart](getting-started/quickstart.md)
* [Engineering Quickstart](getting-started/publish-your-docs.md)

## Basics

* [Triage Error](basics/editor.md)
* [Accounting Integrations](basics/integrations/README.md)
  * [Quickbooks Online](basics/integrations/quickbooks-online/README.md)
    * [Setup](basics/integrations/quickbooks-online/setup.md)
  * [Xero](basics/integrations/xero/README.md)
    * [Setup](basics/integrations/xero/setup.md)
  * [Freshbooks](basics/integrations/freshbooks/README.md)
    * [Setup](basics/integrations/freshbooks/setup.md)
  * [Zoho Book](basics/integrations/zoho-book/README.md)
    * [Setup](basics/integrations/zoho-book/setup.md)
  * [Netsuite](basics/integrations/netsuite/README.md)
    * [Setup](basics/integrations/netsuite/setup.md)
* [OpenAPI](basics/openapi/README.md)
  * ```yaml
    type: builtin:openapi
    props:
      models: true
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: accend-api
    ```

## End User Support

* [Software Connection Support](end-user-support/software-connection-support/README.md)
  * [Page](end-user-support/software-connection-support/page.md)
