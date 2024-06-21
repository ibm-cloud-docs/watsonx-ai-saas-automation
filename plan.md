---

copyright:
  years: 2024
lastupdated: "2024-05-13"

keywords:

subcollection: watsonx-ai-saas-automation

---


{{site.data.keyword.attribute-definition-list}}

# Planning for the watsonx AI SaaS deployable architecture
{: #planning}

By using this deployable architecture, you can create and configure a set of {{site.data.keyword.Bluemix_notm}} services in an {{site.data.keyword.Bluemix_notm}} target account. You can configure access to the {{site.data.keyword.IBM_notm}} watsonx platform for an existing user that's invited in the target account, also known as the {{site.data.keyword.IBM_notm}} watsonx admin. Then, use {{site.data.keyword.Bluemix_notm}} projects as the deployment tool. Complete the following steps before you deploy the watsonx AI SaaS deployable architecture. 
{: shortdesc}

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

1.  Set up target account access with ({{site.data.keyword.iamshort}} (IAM)):
    1.  For compliance with {{site.data.keyword.framework-fs_notm}}: Require users in your account to use [multifactor authentication (MFA)](/docs/account?topic=account-account-getting-started#account-gs-mfa).
    2.  [Set up access groups](/docs/account?topic=account-account-getting-started#account-gs-accessgroups).

User access to {{site.data.keyword.cloud_notm}} resources is controlled by using the access policies that are assigned to access groups. For {{site.data.keyword.cloud_notm}} Financial Services validation, do not assign direct IAM access to any {{site.data.keyword.cloud_notm}} resources. You can set up one access group for the users that can deploy the solution, and one for the {{site.data.keyword.IBM_notm}} watsonx administrators.

### Verify access roles
{: #watsonx-ai-saas-access-roles}

IAM access roles are required to install this deployable architecture and create all the required elements in the {{site.data.keyword.Bluemix_notm}} target account:

- Administrator role on All Account Management services
- Editor platform role on Watson Machine Learning
- Editor platform role on Watson Studio
- Editor platform role Cloud Object Storage
- Editor platform role on watsonx.data
- Editor platform role on watsonx.governance
- Editor platform role on watsonx Assistant
- Editor platform role on Watson Discovery
- Manager service role on the {{site.data.keyword.IBM_notm}} Key Protect instance if you want to enable storage delegation for the Cloud Object Storage instance provisioned with the watsonx AI SaaS deployable architecture.

Additional IAM access roles are required to configure the {{site.data.keyword.IBM_notm}} watsonx administrator in the {{site.data.keyword.Bluemix_notm}} target account:

- Administrator role on All Account Management services
- Administrator role on All Identity and Access enabled services
- Manager service role on Cloud Object Storage to create service credentials. This is not needed if you enable storage delegation for the Cloud Object Storage instance provisioned with the watsonx AI SaaS deployable architecture.

To set up access groups for specific users and use cases, use the [Terraform access group module](https://github.com/terraform-ibm-modules/terraform-ibm-iam-access-group){: external}.
{: tip}

For information about configuring permissions, contact your {{site.data.keyword.cloud_notm}} account administrator.

### Access for {{site.data.keyword.cloud_notm}} projects
{: #watsonx-ai-saas-access-projects}

You should use {{site.data.keyword.cloud_notm}} projects as a deployment option. Projects are designed with infrastructure as code and compliance in mind to help ensure that your projects are managed, secure, and always compliant. For more information, see [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

The {{site.data.keyword.Bluemix_notm}} account where your project is located might be different than the {{site.data.keyword.Bluemix_notm}} target account where you are going to install the watsonx AI SaaS deployable architecture. The following information refers to the permissions you must have in the project account to create a project and create project tools resources within the account. Make sure that you have the following access:

- The Editor role on the Projects service
- The Editor and Manager role on the {{site.data.keyword.bpshort}} service
- The Viewer role on the resource group for the project

For more information, see [Assigning users access to projects](/docs/secure-enterprise?topic=secure-enterprise-access-project).

## Setup the {{site.data.keyword.Bluemix_notm}} projects for deploying in the {{site.data.keyword.Bluemix_notm}} target account
{: #watsonx-ai-saas-projects-prereqs}

Before creating a project to manage the watsonx AI SaaS deployable architecture, you must authorize the deployment.

You can authorize the deployments by [using an API key with Secrets Manager to authorize a project to deploy an architecture](/docs/secure-enterprise?topic=secure-enterprise-authorize-project&interface=ui) or [configuring a trusted profile](/docs/secure-enterprise?topic=secure-enterprise-tp-project&interface=ui) with the {{site.data.keyword.Bluemix_notm}} target account.
