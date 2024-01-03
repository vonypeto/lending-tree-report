# IDOR-Report-Service 
## Summary
- Following a thorough assessment of LendingTree's report service, it has been determined to be not vulnerable.  Specifically, the examination revealed that the system is not susceptible to vulnerabilities associated with insecure direct object references (IDOR). As a result, attempts to exploit such weaknesses through an attack were found to be unfeasible.

## Product
- Product Name: Lending-Tree Website

## Time Taken To Complete Assessment
- 1 hour

## Details
- The API's report service's ability to be exploited with vulnerabilities associated with IDOR was found to be unfeasible due to the fact that the API is based on the request's authorization header. This acts as a barrier, preventing unauthorized access and ensuring the confidentiality of sensitive user information like email addresses. note even the cookies is gone it still show the details with just the auth bearer is there. I have tried every possible scenerio to penetrate this specific endpoint.
