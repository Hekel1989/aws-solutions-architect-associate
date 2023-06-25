# IAM, ACCOUNTS AND AWS ORGANISATIONS

## IAM Identity Policies

IAM Policies are a type of policies that get attached to an Identity within AWS.

*Identities* = IAM Users, IAM Groups, IAM Roles

An IAM Policy is a set of Security Statement to AWS, that grants/deny access to any Identity that uses that Policy.
They're created in JSON, containing multiple statements.

![IAMPolicies-1](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMPolicies-1.png?raw=true)

> **IMPORTANT** If there are multiple statements in a Policy, then **ALL** statements will be processed and applied.
These rules are applied with a defined priority:

1. Explicit Deny
2. Explicit Allow
3. Implicit Deny

If Identities are not explicitly allowed access, then they're not allowed allowed any access to anything.
**Exception** = Root Account

![IAMPolicies-2](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMPolicies-2.png?raw=true)

There are 2 main types of policies:

1. Inline Policies
    - Individual JSON, applied individually to an Identity
    - Used for exceptions to any standard scenario
2. Managed Policies
    - Policy that can be attached to any Identity that might need them.
    - Should be used as a Default
    - They are Reusable
    - They offer Low Management Overhead

![IAMPolicies-3](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMPolicies-4.png?raw=true)

## IAM Users and ARNs

IAM users are an Identity use for anything requiring AWS Access. e.g. Humans, Applications, Service Accounts.

IAM starts with a *principal*.

A *principal* can be anything, but in order to be able to do anything, it needs to authenticate against an Identity within IAM.
Authentication is done via *Username and Password* or *Access Keys*.
Once a principal authenticates, it's now an *authenticated identity*.

Once it's an *authenticated identity*, then it will have to be authorised via *policies* applied to it.

![IAMUsers-1](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMUsers-1.png?raw=true)

### Amazon Resource Names (ARNs)

ARNs uniquely identify resources within any AWS Account.

ARNs are connection of fields, split by a colon. If you see a double colon, then it mean that that specific field doesn't need to be specified.

A * can be used, which is a wildcard.

![ARN-1](https://github.com/acantril/aws-sa-associate-saac03/blob/main/0600-IAM_ACCOUNTS_ORGS/00_LEARNINGAIDS/IAMUsers-2.png?raw=true)

> The top ARN refers to the **Bucket**
> The bottom ARN refers to the **Objects** in the bucket, and **NOT** the Bucket itself.

### Exam PowerUps

- Max 5000 IAM users per AWS Account
- a IAM User can be a member of 10 IAM Groups

