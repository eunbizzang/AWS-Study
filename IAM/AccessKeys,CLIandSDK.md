### How can users access AWS?
- To access AWS you have three options:
  - AWS Management Console (protected by password + MFA)
  - AWS Command Line Interface (CLI) : protected by access keys
  - AWS Software Developer Kit (SDK) - for code: protected by access keys
- Access Keys are generated through the AWS Console
- Users manage their own access keys
- Access Keys are secret, just like a password. Don't share them
- Access Key ID ~ = username
- Secret Access Key ~= password

**Use Access Keys for Programmatic Access(CLI/SDK)**

### What's the AWS CLI?
- A tool that enables you to interact with AWS services using commands in your ocmmand-line shell
- Direct access to the public APIS of AWS services
- You can develop scripts to manage your resources
- It's open-source https://github.com/aws/aws-cli
- Alternative to using AWS Management Console

### What's the AWS SDK?
- AWS Software Development Kit (AWS SDK)
- Language-specific APIs (set of libraries)
- Enables you to access and manage AWS services programmatically
- Embedded within your application
- Supports
  - SDKs(JavaScript, Python, PHP, .NET, Ruby, Java, Go, Node.js, C++)
  - Mobile SDKs(Android, iOS,,,)
  - IoT Device SDKs(Embedded C, Arduino,,,)
- Example: AWS CLI is built on AWS SDK for Python