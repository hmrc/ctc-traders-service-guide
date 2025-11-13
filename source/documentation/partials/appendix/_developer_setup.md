To develop using the CTC Traders API, traders or their software providers must:

- Possess familiarity with HTTP, RESTful services, XML, and OAuth2.
- Register as a developer on the HMRC Developer Hub.
- Create at least one sandbox application on the Developer Hub.

Each registered application will receive a unique HMRC ApplicationId. All registered applications can be viewed and managed on the Developer Hub Applications page, where API subscriptions and application credentials can be administered.


Applications may be created in one of two environments:

- Sandbox Environment: Used for initial development and testing of software.
- Production Environment: Upon readiness to go live, request ‘Production Credentials’ to create a new application (with a new ApplicationId) in the production environment.

Key differences between the two environments include:

- In the sandbox environment, test users must be created and used to call the API endpoints.
- The release version of an API in the sandbox is typically ahead of the version in the production environment.

The sandbox environment (also known as External Test) serves as an HMRC platform for external partners to complete required assurance activities, ensuring confidence in their readiness for migration to NCTS.

For further details on utilizing sandbox environments, refer to the Testing in the Sandbox documentation.