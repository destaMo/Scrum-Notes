# IAM

Securely manage access to AWS services and resources.

- helps create and manage user identities and grant permissions for those users to access AWS resources
- helps create groups for multiple users with similar permissions
- not appropriate for application authentication
- is Global and does not need to be migrated to a different region
- helps define Policies:
  - in JSON format
  - all permissions are implicitly denied by default
  - most restrictive policy wins
- **IAM Role**
  - helps grants and delegate access to users and services without the need of creating permanent credentials
  - IAM users or AWS services can assume a role to obtain temporary security credentials that can be used to make AWS API calls
  - needs Trust policy to define who and Permission policy to define what the user or service can access
  - used with Security Token Service (STS), a lightweight web service that provides temporary, limited privilege credentials for IAM users or for authenticated federated users
- **IAM Best Practices**
  - Do not use Root account for anything other than billing
  - Create Individual IAM users
  - Use groups to assign permissions to IAM users
  - Grant least privilege
  - Use IAM roles for applications on EC2
  - Delegate using roles instead of sharing credentials
  - Rotate credentials regularly
  - Use Policy conditions for increased granularity
  - Use CloudTrail to keep a history of activity
  - Enforce a strong IAM password policy for IAM users
  - Remove all unused users and credentials

## Use scenarios

- [Providing Access Across AWS Accounts](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_federated-users.html)
- [Providing Access to Third-Party AWS Accounts](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_third-party.html)
- [Providing Access to AWS Services](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_services.html)
- [Providing Access Through Identity Federation](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_common-scenarios_federated-users.html)

> [Service overview](https://aws.amazon.com/iam/)
