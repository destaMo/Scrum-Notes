# Organizations

AWS Organizations offers policy-based management for multiple AWS accounts. With Organizations, you can create groups of accounts, automate account creation, apply and manage policies for those groups. Organizations enables you to centrally manage policies across multiple accounts, without requiring custom scripts and manual processes.

Using AWS Organizations, you can create Service Control Policies (SCPs) that centrally control AWS service use across multiple AWS accounts. You can also use Organizations to help automate the creation of new accounts through APIs. Organizations helps simplify the billing for multiple accounts by enabling you to setup a single payment method for all the accounts in your organization through consolidated billing. AWS Organizations is available to all AWS customers at no additional charge.

## Use scenarios

- **control the use of AWS services to help comply with corporate security and compliance polices**
  - AWS Organizations’ Service Control Policies (SCPs) help you centrally control AWS service use across multiple AWS accounts in your organization. With Organizations, you can ensure that entities in your accounts can use only the services that meet your corporate security and compliance policy requirements. For example, you can restrict the use of AWS services that can modify settings for shared resources, such as AWS Direct Connect or Amazon Virtual Private Cloud (VPC) settings.
- **automate the creation of AWS accounts for different resources**
  - AWS Organizations makes it easy for you to automate the creation of new AWS accounts used for different resources. With a few simple API calls, you can create a new account and add the new account to a group. You can attach a Service Control Policy (SCP) to that group that only allows the use of the necessary AWS services. Through consolidated billing, you can automatically link the new accounts to a single payment method for simplified billing.
- **create different groups of accounts for development and production resources**
  - Creating groups of AWS accounts helps you manage policies across your accounts centrally. For example, you can create separate groups of accounts used for development and production resources, and then apply different policies to each group. You can attach a Service Control Policy (SCP) to the development group that allows the use of all AWS services for testing, and attach a different SCP to the production group that only allows access to authorized services.

> [Organizations overview](https://aws.amazon.com/organizations/)
