The base URLs of the sandbox and production environments are as follows.

| Environments | Base URL                              |
|--------------|---------------------------------------|
| Sandbox      | https://test-api.service.hmrc.gov.uk/ |
| Production   | https://api.service.hmrc.gov.uk/      |

The following table relates NCTS message types to API endpoints.


| Message types       | Action                                                             | Description                            |
|---------------------|--------------------------------------------------------------------|----------------------------------------|
| IE015               | POST /customs/transits/movements/departures                        | Send a declaration data message.       |
| IE013, IE014, IE170 | POST /customs/transits/movements/departures/{departureId}/messages | Send a message related to a departure. |
| IE007               | POST /customs/transits/movements/arrivals                          | Send an arrival notification message.  |
| IE044               | POST /customs/transits/movements/arrivals/{arrivalId}/messages     | Send a message related to an arrival.  |