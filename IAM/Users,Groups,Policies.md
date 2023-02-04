### Users and Groups
- IAM = Identity and Access Management, Global service
- Root account created by default, shouldn't be user or shared
- Users are people within your organization, and can be grouped
- Groups only contain users, not other groups
- Users don't have to belong to a group, and user can belong to multiple groups

### Permissions
- Users or Groups can be assigned JSON documents called policies
- These policies define the permissions of the users
- In AWS you apply the least privilege principle: don't give more permissions than a user needs


### Permissions
- Consists of
  - Version:policy language version, always include "2012-10-17"
  - Id:an identifier for the policy(optional)
  - Statement: one or more individual statements(required)
- Statements consists of
  - Sid: an identifier for the statement(optional)
  - Effect: whether the statement allows or denies access
    (Allow, Deny)
  - Principal: account/user/role to which this policy applied to
  - Action: list of actions this policy allows or denies
  - Resource: list of resources to which the actions applied to
  - Condition: conditions for when this policy is in effect
    (optional)

**A statement in an IAM Policy consists of Sid, Effect, Principal, Action, Resource, and Condition. Version is part of the IAM Policy itself, not the statement**

AdministratorAccess
![image](https://user-images.githubusercontent.com/70651994/216773134-53f66abb-d393-4545-83ff-d9ddd97258e8.png)

IAMReadOnlyAccess
![image](https://user-images.githubusercontent.com/70651994/216773204-38d35101-b6fe-414d-9210-b5019c3e4ac0.png)