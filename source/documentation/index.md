---
title: CTC Traders Service Guide
weight: 1
description: Service Guide for the CTC Traders API
---

# CTC Traders Service Guide

Version 1.0 issued 18 November 2025
***

## Service overview

Common Transit Convention Traders API is a public API for 3rd Party Software Developers.
It is a government digital service that allows the submission of NCTS transit events
(i.e. Arrival and Departure details). The CTC API will submit the IE (XML) message to
the NCTS Enterprise Integration Service (EIS) in the NCTS core application.
The NCTS core application will validate the message received and respond with the appropriate
IE (XML) message, using an asynchronous pattern. The XML API has been designed to help support
the front end web channel by facilitating a larger volume of transit events.

## API overview

The CTC Traders API is based on REST principles with endpoints that return data in JSON format and it uses standard HTTP
error response codes.

Use the API to:

- send departure and arrival movement notifications to the New Computerised Transit System (NCTS)
- retrieve messages sent from customs offices of departure and destination

You can use this version of the API to send both small (up to 5MB in size) and large (up to 8MB in size) messages. The
large messages capability applies only to POST endpoints.

The API endpoints relate only to Great Britain and Northern
Ireland. You can also use
the [HMRC sandbox environment](https://test-developer.service.hmrc.gov.uk/api-documentation/docs/sandbox/introduction)
to run tests for Great Britain and Northern Ireland transit movements.

## Pre-requisites (NCTS subscription)

For information about upgrading an NCTS subscription,
see [How to subscribe to the New Computerised Transit System](https://www.gov.uk/guidance/how-to-subscribe-to-the-new-computerised-transit-system).

[Contact the NCTS Helpdesk](https://www.gov.uk/government/organisations/hm-revenue-customs/contact/new-computerised-transit-system-enquiries)
if you need any help or advice when using the NCTS.

## Getting started

1. Review this entire document before consulting other NCTS documents.
2. Follow the Pre-requisites
3. Review [Trader data](#trader-data).
4. Set up [Developer Account](https://developer.service.hmrc.gov.uk/)
5. Review [Making API requests](https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/common-transit-convention-traders).

### Trader data

Traders working with a software house must register with
the [Government Gateway](https://www.access.service.gov.uk/login/signin/creds) to access
the [CTC Traders API](https://www.tax.service.gov.uk/customs-enrolment-services/ctc/subscribe?_gl=1*itulmt*_ga*MjA2MDk0MTQyMi4xNjY3Mzk2ODM5*_ga_Y4LWMWY6WS*MTY3NDgyMzU5OC41MS4xLjE2NzQ4NDE2NzcuMC4wLjA.&_ga=2.207635798.536493967.1674469117-2060941422.1667396839)
and provide the software house with the required details, as follows:

- GB Economic Operators Registration and Identification (EORI) number
- VAT details (optional)
- Standard Industrial Classification (SIC) code
- company or organisation details:
- unique tax reference (UTR) number
- registered company name (this must be an exact match)
- registered company address
- date of company establishment
- email address
- contact details

### First-time Users

Traders new to the CTC Traders API must follow these steps:

- Confirm possession of an HMRC [developer account](https://developer.service.hmrc.gov.uk/developer/login). If none
  exists, [register for an account](https://developer.service.hmrc.gov.uk/developer/registration), activate it via
  email, and sign in.
- Add a subscription to the CTC Traders API within the application software.
- Understand the
  user-restricted [authentication](https://developer.service.hmrc.gov.uk/api-documentation/docs/authorisation/user-restricted-endpoints)
  implemented by the API.
- [Create an application](https://developer.service.hmrc.gov.uk/developer/applications/) in the sandbox environment.
- Utilize
  the [Create Test User API](https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/api-platform-test-user/1.0)
  to generate one or more test users for the sandbox application.
- Download [NCTS reference data](https://ec.europa.eu/taxation_customs/dds2/rd/rd_download_home.jsp?Lang=en) for testing
  purposes.

Consult the CTC Traders API testing guide to verify software compatibility with this API version and to understand
testing procedures in the sandbox environment.

### Existing Users

Traders upgrading their existing API must take the following actions:

- Review this section before consulting other NCTS documentation.
- Determine if Trader data applies to any traders served, as affected traders will need to act accordingly.
- Review the Technical Interface Specification (TIS) for updated content.
- Review the guidelines for making API requests.
- Evaluate the test scenarios from testing guide.

## High level functional interaction map

<img src="../figures/e2e.drawio.svg" alt="Declaration amendment accepted/rejected. Flow is described in this section." />
<a href="../figures/e2e.drawio.svg" target="_blank">Open the diagram in a new tab.</a>

## API Definitions

[Definitions](https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/common-transit-convention-traders)
for endpoints, example requests and schema definitions.
