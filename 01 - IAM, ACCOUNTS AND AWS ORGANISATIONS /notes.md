# IAM, ACCOUNTS AND AWS ORGANISATIONS

## IAM Identity Policies

---

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

---