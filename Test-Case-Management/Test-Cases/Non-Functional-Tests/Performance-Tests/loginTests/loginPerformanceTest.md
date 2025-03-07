### Login Test Performance Test - Web App
**ID:**

**Title:** Measure login response time on the web application
*Description:* Measures the time it takes for a user to successfully login to the web application

*Preconditions:*
* The web app is deployed and running
* Multiple test users with valid credentials has been created and activated
* The Test users' email address is accessible to the Tester
* Tester has access to the testing environment
* Performance testing tools *(e.g., JMeter, WebPageTest) are set up.*

**Steps:**
1. Using a performance testing tool, simulate multiple users attempting to login to the web application concurrently.
2. Measure the `average`, `minimum`, and `maximum` login response times.
3. Record the # of successful and failed login attempts
4. Monitor server resource utilization, such as CPU, memory, network during the test.

**Expected Results:**
* Average login response time is below [defined acceptable threshold] seconds
* Maximum login response time does not exceed [defined acceptable threshold] seconds
* Server resource utilization remains within acceptable limitis

**Actual Results:**
*(to be filled out during testing)*
**Status:** *(e.g., Pass, Fail, Retest, In Progress)*
**Notes:** *(Additional information/ notes)*
