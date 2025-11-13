The CTC Traders API (any version) supports two routes for transmitting messages to the NCTS. Traders may select, on a
per-message basis, either the large message route or the small message route for sending messages.

### Differences between large and small message routes

The following table summarises the main differences between the large and small routes supported by the API.

| Attribute              | Large message route                      | Small message route           |
|------------------------|------------------------------------------|-------------------------------|
| Message size limit     | 8MB                                      | 5MB                           |
| Submission type        | File-based                               | Direct                        |
| Messaging type         | Asynchronous                             | Synchronous                   |
| Successful message     | Near real time (with push notifications) | Immediate submission feedback |
| Timeout resilience     | Strong                                   | Weak                          |
| Transit size (average) | Large                                    | Small                         |

### Determining Which Message Route to Use

Traders handling transit movements with large consignments should consider using the large message route. Before
finalizing how application software will manage message sizes, the following factors should be evaluated:

- The large message route supports both large and small messages, but only the POST endpoints of the CTC Traders API accommodate the large message route, while all GET endpoints can process messages of any size.
- For traders or those they serve, prioritizing quick response times from the NCTS, and whose message sizes do not exceed 5MB, the small message functionality of the API should be used exclusively.

When opting for the large message route, traders may leverage the [Push Pull Notifications API](https://developer.service.hmrc.gov.uk/api-documentation/docs/api/service/push-pull-notifications-api/1.0) to receive automatic notifications from the NCTS in near real-time.

### Sending Large Messages

To transmit a transit declaration via the large message route, traders must call the API with an empty payload.
A successful response will include:

- A URL and additional metadata required for uploading the file.
- A message ID to track the status of the specific message.

For further details on sending large messages, refer to the Upload Files for Large Messages documentation.