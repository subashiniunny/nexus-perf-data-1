# Scenario 02

**UNREALISTIC SCENARIO: AVOID IT'S USE UNLESS ON PURPOSE**

Kinda a "deploying" scenario, it deploys artifact to newly 
created repository and then drops the repository. Not very 
representative, given create and drop of repositories are
"heavy" operations and it saturates the tasks and event bus.
Creating/Dropping repositories with NX2 will never likely
to happen several times per second on an instance, you have
some problem if you do try to do that.

Duration: 15 minutes

Swarms:
* Deploys 5 artifact in newly created repository, then drop it
  * Clients: 120
  * Rate: 5/s
