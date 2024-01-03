# IDOR-email-disclosure readme.md
## Summary
- A serious vulnerability has been identified in LendingTree's platform during a thorough assessment. The platform lacks proper validation when new users enter an email address that is already associated with an existing account, leading to the potential disclosure of sensitive information.

## Product
- Product Name: Lending-Tree Website

## Time Taken To Complete Assessment
- 2 hours

## Proof of Concept (POC)
1. On a normal browser do the normal form as usual followed in the video first do the with the existing email
2. once finished go to the profile and it will redirect you to login meaning to email exist also it record loan it on his/her email the form
2. On a different browser session, as a new user, try using the e-mail address not associated with the existing account.
3. then go to the profile it will not logout you meaning it still new 

## Details
- Upon assessment, it was uncovered that the platform fails to notify new users attempting to register with an email address already linked to an existing account. Despite this, these new users can proceed to request a loan, and their actions are recorded under the original account holder's profile. The issue persists until the new user attempts to access the website's profile page, which triggers their logout. This oversight poses a significant risk of unintentional data exposure and can potentially compromise user privacy and security. A video is included for reference. I have done all necessary exploit and this is the close to the requested exploit that you want.

## Impact
- Unauthorized Access: The ability to fetch data and write data from any user compromises user privacy, which may be in violation of data protection regulations.
- Trust Degradation: Users may lose trust in the platform if they become aware that their accounts and records can be accessed and modified easily by other users.

## Remediation
- Proper User Validation: It is recommended to implement proper validation during account registration to notify new users if they have entered an email address that is already associated with an existing account. Then the system should prompt users to verify their identity or select a different email address to prevent unintended access or verify if user is existed before proceeding.
