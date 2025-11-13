Common Transit Convention Traders API is a public API for 3rd Party Software Developers.
It is a government digital service that allows the submission of NCTS transit events
(i.e. Arrival and Departure details). The CTC API will submit the IE (XML) message to
the NCTS Enterprise Integration Service (EIS) in the NCTS core application.
The NCTS core application will validate the message received and respond with the appropriate
IE (XML) message, using an asynchronous pattern. The XML API has been designed to help support
the front end web channel by facilitating a larger volume of transit events.