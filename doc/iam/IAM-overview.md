# AWS Identity and Access Management (IAM)

AWS Identity and Access Management (IAM) is a web service offered by Amazon Web Services (AWS) that helps you securely control access to AWS resources for your users. IAM enables you to manage users, security credentials such as access keys, and permissions that control which AWS resources users can access, all from a central location.

> Any AWS customer can use IAM; the service is offered at no additional charge (global service)

### Authentication vs. Authorization

- Authentication is the process of validating that users are who they claim to be.
- Authorization is the process of giving the user permission to access a specific resource or function.

> You should establish a principle of least privilege to ensure that only authenticated users are permitted to perform only the most minimal functions to complete a specific task. 

## Users, Groups, Roles and Policies

### Users:

These are the entities that interact with AWS resources. A user could be a `person` or `system` that needs to use services in your AWS account.

Can be assigned:

- Access to the AWS Management Console.
- An access key ID and secret access key are used for programmatic access to the AWS API, CLI, and SDK.

### Groups

Groups are collection of users and have `policies` attached to them (use groups to assing permissions to users).

- Groups cannot belong to groups.
- A group is not an identity and cannot be identified as a principal in an IAM policy.
- Use the principal of least privilege when assigning permissions.


> Users dont' have to belong to a group, and user can belong to multiple groups.


### Roles 

Roles are a secure way to `delegate` permissions without providing security credentials.

> Some AWS services need to perform actions on your behalf. To do so, you assign permissions to AWS services with IAM Roles.