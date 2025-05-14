# Table of contents

* [Welcome](README.md)

## Getting Started

* [Dashboard Quickstart](getting-started/quickstart.md)
* [Engineering Quickstart](getting-started/publish-your-docs.md)

## Basics

* [Triage Error](basics/editor.md)
* [ERP Integrations](basics/integrations/README.md)
  * [Quickbooks Online](basics/integrations/quickbooks-online.md)
  * [Xero](basics/integrations/xero.md)
  * [Freshbooks](basics/integrations/freshbooks.md)
  * [Zoho Book](basics/integrations/zoho-book.md)
  * [Netsuite](basics/integrations/netsuite.md)
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
