---

copyright:
  years: 2024
lastupdated: "2024-03-29"

keywords:

subcollection: watsonx-ai-saas-automation

---


{{site.data.keyword.attribute-definition-list}}

# Planning for the Watsonx AI SaaS deployable architecture
{: #planning}

By the mean of the deployable architecture, you are going to create and configure a set of IBM Cloud services in an IBM Cloud target account.
Then, you are going to configure access to the IBM watsonx platform for an existing user invited in the target account (IBM watsonx admin).
You are going to use IBM Cloud projects as deployment tool. So, complete the following steps before you deploy the Watsonx AI SaaS deployable architecture. {: shortdesc}

## Confirm your {{site.data.keyword.cloud_notm}} target account settings
{: #watsonx-ai-saas-cloud-prereqs}

1.  Confirm or set up the {{site.data.keyword.cloud_notm}} target account:

    Make sure that you have an {{site.data.keyword.cloud_notm}} Pay-As-You-Go or Subscription account:

    - If you don't have an {{site.data.keyword.cloud_notm}} account, [create one](/docs/account?topic=account-account-getting-started).
    - If you have a Trial or Lite account, [upgrade your account](/docs/account?topic=account-upgrading-account).

2.  Configure your {{site.data.keyword.cloud_notm}} target account:
    1.  Log in to [{{site.data.keyword.cloud_notm}}](https://cloud.ibm.com) with the {{site.data.keyword.ibmid}} you used to set up the account. This {{site.data.keyword.ibmid}} user is the account owner and has full IAM access.
    2.  [Complete the company profile](/docs/account?topic=account-contact-info) and contact information for the account. This profile is required to stay in compliance with {{site.data.keyword.cloud_notm}} Financial Services profile.
    3.  [Enable the Financial Services Validated option](/docs/account?topic=account-enabling-fs-validated) for your account.

## Set the IAM permissions
{: #watsonx-ai-saas-iam-prereqs}

1.  Set up target account access ({{site.data.keyword.iamshort}} (IAM)):
    1.  For compliance with {{site.data.keyword.framework-fs_notm}}: Require users in your account to use [multifactor authentication (MFA)](/docs/account?topic=account-account-getting-started#account-gs-mfa).
    2.  [Set up access groups](/docs/account?topic=account-account-getting-started#account-gs-accessgroups).

        User access to {{site.data.keyword.cloud_notm}} resources is controlled by using the access policies that are assigned to access groups. For {{site.data.keyword.cloud_notm}} Financial Services validation, do not assign direct IAM access to any {{site.data.keyword.cloud_notm}} resources.

        You should setup one access group for the solution deployers, and one for the IBM watsonx admins.

### Verify access roles
{: #watsonx-ai-saas-access-roles}

IAM access roles are required to install this deployable architecture and create all the required elements in the IBM Cloud target account:

- All Account Management services
  - Administrator (only if you must create a new resource group)
- Watson Machine Learning
  - Editor platform role (to create and delete the service)
- Watson Studio
  - Editor platform role (to create and delete the service)
- Cloud Object Storage
  - Editor platform role (to create and delete the service)
- watsonx.governance
  - Editor platform role (only if you must provision)
- watsonx Assistant
  - Editor platform role (only if you must provision)
- Watson Discovery
  - Editor platform role (only if you must provision)

Those are the roles you should configure for the deployers access group.

IAM access roles are required to configure the IBM watsonx admin.

You need the following permissions for the IBM watsonx admin in the IBM Cloud target account:

- All Account Management services
  - Administrator
- All Identity and Access enabled services
  - Administrator

Those are the roles you should configure for the IBM watsonx admins access group.

For information about configuring permissions, contact your {{site.data.keyword.cloud_notm}} account administrator.

### Access for {{site.data.keyword.cloud_notm}} projects
{: #watsonx-ai-saas-access-projects}

You should use {{site.data.keyword.cloud_notm}} projects as a deployment option. Projects are designed with infrastructure as code and compliance in mind to help ensure that your projects are managed, secure, and always compliant. For more information, see [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

The IBM Cloud account where your project resides may be different than the IBM Cloud target account, where you are going to
install the Watsonx AI SaaS deployable architecture. The following refers to the permissions you must have in the project account
to create a project and create project tooling resources within the account. Make sure you have the following access:

- The Editor role on the Projects service.
- The Editor and Manager role on the {{site.data.keyword.bpshort}} service
- The Viewer role on the resource group for the project

For more information, see [Assigning users access to projects](/docs/secure-enterprise?topic=secure-enterprise-access-project).

## Setup the IBM Cloud projects for deploying in the IBM Cloud target account
{: #watsonx-ai-saas-projects-prereqs}

Before creating a project to manage the Watsonx AI SaaS deployable architecture,
you must authorize the deployments.

You can do that [using a deployer API key with Secrets Manager](https://cloud.ibm.com/docs/secure-enterprise?topic=secure-enterprise-authorize-project&interface=ui) or
[configuring a trusted profile](https://cloud.ibm.com/docs/secure-enterprise?topic=secure-enterprise-tp-project&interface=ui) with the IBM Cloud target account.
