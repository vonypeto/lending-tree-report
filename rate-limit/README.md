# rate limit readme.md
## Summary
- A serious vulnerability has been discovered following a thorough assessment of LendingTree's platform where attackers are able to issue a large volume of requests in a short amount of time which could exhaust system resources and allow DOS attacks.

## Product
- Product Name: Lending-Tree Website

## Time Taken To Complete Assessment
- 1 hour

## Details
- Following the assessment, it has been found that attackers can issue over 22,000 requests to the platform within a matter of a second. This can potentially crash the service or at least degrade its performance. An image has been attached for reference.

## Proof of Concept (POC)
To replicate the issue, recreate the following steps:
1. Download and use an interception tool, one example is Burp Suite.
2. Using the tool, intercept any request and send it to the tool's intruder. 
3. Using the intruder, we are able to send the intercepted request repeatedly, until we choose to stop it.
4. Issuing this attack will result in the amount of requests similar to the reference image.

## Impact
- Service Disruption: The primary impact of this vulnerability is the possibility of the service crashing or becoming unresponsive. This can lead to Denial of Service (DoS) attacks, affecting all users of the platform, as it puts an undue burden on the system's memory and processing capabilities.
- Resource Exhaustion: Repeated exploitation of this vulnerability can cause resource exhaustion on the server. This could lead to higher operational costs as the server struggles to handle an excessive number of requests, and it may also decrease the overall system longevity.

## Remediation
- Rate Limiting: It is recommended to implement rate-limiting mechanisms to control the number of requests that can be made within a specific timeframe. This can help prevent abuse of the system by limiting the frequency and volume of requests that can be sent by a single user or IP address.

