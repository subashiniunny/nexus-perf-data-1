# Scenario 03

Simple "consuming" scenario with proxy being pushed too, only pulls artifacts from Nexus
while in same time produces "fake" requests (resulting all of it in 404) to keep proxy
busy and fill NFC.

Duration: 15 minutes

Swarms:
* Consume Apache Maven 3.3.4 dependencies
  * Clients: 120
  * Rate: 5/s
* Consume Apache Maven 3.1.0 dependencies
  * Clients: 120
  * Rate: 5/s
* Create fluke requests
  * Clients: 120
  * Rate: 5/s
