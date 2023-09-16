## IAM Policies (Authorization)

To manage access and provide permissions to AWS services and resources, you create IAM policies and attach them to IAM users, groups, and roles.

> All permissions are implicity denied by default.

### Sample Policy

IAM Policies are JSON documents used to describe permissions within  AWS.

```json
{
    "Version": "2012-10-17",
    "Statement": {
        "Sid": "AllowRemoveMfaOnlyIfRecentMfa",
        "Effect": "Allow",
        "Action": [
            "iam:DeactivateMFADevice"
        ],
        "Resource": "arn:aws:iam::*:user/${aws:username}",
        "Condition": {
            "NumericLessThanEquals": {"aws:MultiFactorAuthAge": "3600"}
        }
    }
}
```

#### Key Elements of IAM Policy Structure

- `Version`: Specifies the version of the IAM policy language in use. It's recommended to always use the most up-to-date version for enhanced security and features.

- `Statement`: Serves as the overarching container for individual policy statements. Each statement defines a single permission, and multiple statements can be included within this element.

- `Sid (Statement ID)`: An optional component that allows for the labeling of individual statements, making it easier to manage and reference them.

- `Effect`: Dictates the outcome of the policy statement, which can either be Allow or Deny. This element is crucial for setting the permissions associated with the policy.

- `Action`: Enumerates the specific AWS actions that are permitted or denied by the policy. This could range from reading an S3 bucket to launching an EC2 instance.

- `Resource`: Lists the AWS resources to which the policy is applicable. In the context of resource-based policies, this element is optional, as the policy is inherently tied to the resource it is attached to.

- `Principal`: Identifies the AWS users, roles, or services that are granted or denied access through resource-based policies. This element is essential for specifying who can interact with the resources.

- `Condition`: Sets conditional logic for when the policy should be applied. This is particularly useful for implementing fine-grained access controls based on factors like IP address, time of day, or other attributes.


### Policy Simulator

The AWS Identity and Access Management (IAM) Policy Simulator is a tool provided by AWS to help you understand, test, and validate how IAM policies will behave under different scenarios. It allows you to simulate real-world access situations to evaluate the impact of IAM policies on resource access within your AWS environment.

> Your security team and administrators can use IAM Access Analyzer to identify resources that can be accessed from outside an AWS account. 

https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies_testing-policies.html