## IAM - Password Policy

- Strong passwords = higher security
- In AWS, you can setup a password policy:
  - Set a minimum password length
  - Require specific character types:
    - including uppercase letters
    - lowercase letters
    - numbers
    - non-alphanumeric characters
  - Allow all IAM users to change their own passwords
  - Require users to change their password after some time (password expiration)
  - Prevent password re-use

### MFA: Multi-Factor Authentication
- Users have access to your account and can possibly change

  Configurations or delete resources in your AWS account
- You want to protect your Root Accounts and IAM users
- MFA = password you know + security device you own
- Main benefit or MFA:

  if a password is stolen or hacked, <u>the account is not compromised</u>

### MFA devices options in AWS
- Virtual MFA device
  - Google Authenticator(phone only)
  - Authy(multi-device)

  Support for multiple tokens on a single device.
- Universal 2nd Factor(U2F) Security Key
  - YubiKey by Yubico(3rd party)  

  Support for multiple root and IAM users using a single security key
- Hardware Key Fob MFA Device
  - Provided by Gemalto(3rd party)
- Hardware Key Fob MFA device for AWS GovCloud(US)
  - Provided by SurePassID(3rd party)