---

copyright:
  years: 2024
lastupdated: "2024-05-09"

subcollection: watsonx-ai-saas-automation

keywords:

---

{{site.data.keyword.attribute-definition-list}}

# Understanding your responsibilities when you use watsonx AI SaaS
{: #responsibilities}

Learn about the management responsibilities and terms and conditions that you have when you use the watsonx AI SaaS deployable architecture.
{: shortdesc}

- For more information about the responsibilities for you and {{site.data.keyword.IBM}} when you use a deployable architecture, see [Understanding your responsibilities when you use deployable architectures](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures).
- For a high-level view of the service types in {{site.data.keyword.cloud}} and the breakdown of responsibilities between the customer and {{site.data.keyword.IBM_notm}} for each type, see [Shared responsibilities for using {{site.data.keyword.cloud}} products](/docs/overview?topic=overview-shared-responsibilities).
- For the overall terms of use, see [{{site.data.keyword.cloud_notm}} Terms and Notices](/docs/overview/terms-of-use?topic=overview-terms).

Review the following sections for the specific responsibilities for you and {{site.data.keyword.IBM_notm}} when you use the watsonx AI SaaS deployable architecture.

## Incident and operations management
{: #incident-and-ops}

Incident and operations management includes tasks such as monitoring, event management, high availability, problem determination, recovery, and full state backup and recovery.

The watsonx AI SaaS deployable architecture does not identify specific responsibilities in this area. For information about the general change management responsibilities when you use IBM deployable architectures, see [Incident and operations management](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures#incident-and-ops-da).

## Change management
{: #change-management}

Change management includes tasks such as deployment, configuration, upgrades, patching, configuration changes, and deletion.

The watsonx AI SaaS deployable architecture does not identify specific responsibilities in this area. For information about the general change management responsibilities when you use IBM deployable architectures, see [Change management](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures#change-management-da).


## Identity and access management
{: #iam-responsibilities}

Identity and access management includes tasks such as authentication, authorization, access control policies, and approving, granting, and revoking access.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|------|-------------------------------------------------|-----------------------|
| Secure with least privilege | Document the minimal IAM access requirements to run the deployable architecture. |  |
| Manage secrets | | * Generate the necessary secrets (IAM API keys) and configure trusted profiles that are required for the deployable architecture. \n * Manage generated secrets by following secure best practices. |
{: row-headers}
{: caption="Table 1. Responsibilities for identity and access management" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Security and regulation compliance
{: #security-compliance}

Security and regulation compliance includes tasks such as security controls implementation and compliance certification.

| Task | {{site.data.keyword.IBM_notm}} responsibilities | Your responsibilities |
|------|-------------------------------------------------|-----------------------|
| Meet security and compliance objectives | Provide a deployable architecture that complies with the set of controls that are defined with the release of the deployable architecture. The controls in the deployable architecture do not necessarily cover the complete profile for the {{site.data.keyword.framework-fs_notm}}, as shown in the [Available predefined profiles](/docs/security-compliance?topic=security-compliance-predefined-profiles).
| Verify configuration changes | | Understand the effects on the security and compliance posture of any user-initiated changes to the default configuration. Run {{site.data.keyword.compliance_long}} checks if needed to ensure that the deployable architecture remains in compliance. |
{: row-headers}
{: caption="Table 2. Responsibilities for security and regulation compliance" caption-side="bottom"}
{: summary="The rows are read from left to right. The first column describes the task that the customer or IBM might be responsible for. The second column describes {{site.data.keyword.IBM_notm}} responsibilities for that task. The third column describes your responsibilities as the customer for that task."}

## Disaster recovery
{: #disaster-recovery}

Disaster recovery includes tasks such as providing dependencies on disaster recovery sites, provisioning disaster recovery environments, data and configuration backup, replicating data and configuration to the disaster recovery environment, and failover on disaster events.

The watsonx AI SaaS deployable architecture does not identify specific responsibilities in this area. For information about the general BCDR responsibilities when you use IBM deployable architectures, see [Disaster recovery](/docs/secure-enterprise?topic=secure-enterprise-responsibilities-deployable-architectures#disaster-recovery-da).
