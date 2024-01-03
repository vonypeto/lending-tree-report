# iframe-hijack readme.md
## Summary
- Following a thorough assessment of LendingTree's report service, it has been determined to be not vulnerable to Clickjacking (UI redressing) attacks, a malicious technique that can mislead a user into clicking on a different target than what they perceive, potentially resulting in inadvertent disclosure of sensitive information or control over their interactions.

## Product
- Product Name: Lending-Tree Website

## Time Taken To Complete Assessment
- 30 minutes

## Proof of Concept (POC)
1. To replicate a similar attack, an HTML file has been provided for reference, host the HTML file.

## Details
- The platform's ability to be exploited with vulnerabilities associated with  Clickjacking was found to be unfeasible due to the fact that the X-Frame-Options header exists when requests are issued. When we include the X-Frame-Options header, the platform instructs the web browser to deny attempts at embedding the website with an iframe, which mitigates the risk of unauthorized framing. 

