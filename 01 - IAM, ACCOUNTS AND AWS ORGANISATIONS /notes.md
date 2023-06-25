# IAM, ACCOUNTS AND AWS ORGANISATIONS

## IAM Identity Policies

IAM Policies are a type of policies that get attached to an Identity within AWS.

*Identities* = IAM Users, IAM Groups, IAM Roles

An IAM Policy is a set of Security Statement to AWS, that grants/deny access to any Identity that uses that Policy.
They're created in JSON, containing multiple statements.

![IAMPolicies-1](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMPolicies-1.png?raw=true)

**IMPORTANT** If there are multiple statements in a Policy, then **ALL** statements will be processed and applied.
These rules are applied with a defined priority:

1. Explicit Deny
2. Explicit Allow
3. Implicit Deny

If Identities are not explicitly allowed access, then they're not allowed allowed any access to anything.
**Exception** = Root Account

![IAPolicies-2](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMPolicies-2.png?raw=true)