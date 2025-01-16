---

copyright:
  years: 2024
lastupdated: "2024-04-18"

keywords:

subcollection: watsonx-ai-saas-automation

content-type: release-note

---

{{site.data.keyword.attribute-definition-list}}

# Release notes for Watsonx.ai SaaS with Assistant and Governance deployable architecture
{: #release-notes}

Use these release notes to learn about the latest updates to Watsonx.ai SaaS with Assistant and Governance deployable architecture that are grouped by date. Release notes are available for a minimum of three years.
{: shortdesc}

## January 2025
{: #subcollection-jan2025}

### 16 January 2025
{: #subcollection-16jan2025}
{: release-note}

Version 1.9.2 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.9.2 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - Fixed bug where incorrect api endpoint was being used for the `eu-gb` region.
    - Update the scope of the KMS auth policy so that it is now scoped to the exact KMS key. Updating to this version from a previous version will see the destroy and recreate of the auh policy, however the new policy will be created before the old one so there will be no disruption to every day serivces during upgrade.
    - Controls in the {{site.data.keyword.compliance_long}} Framework for Financial Services profile version 1.7.0 that pass validation are now displayed.
    - Exposed the ability to set the `provider_visibility`. The default value is now `private`. [Learn more](https://registry.terraform.io/providers/IBM-Cloud/IBM/latest/docs#visibility-1).
    - The IBM terraform provider has been updated to version 1.71.3
    - A new input `enable_cos_kms_encryption` has been added to toggle KMS encryption with default value of `true`.
        - When value is set to `true`, a value must be passed for the `cos_kms_crn` input. 
    - A new input `watsonx_mark_as_sensitive` has been added which can be used to allow the WatsonX project to be created with 'Mark as sensitive' flag.

## September 2024
{: #subcollection-sep2024}

### 11 September 2024
{: #subcollection-11sep2024}
{: release-note}

Version 1.6.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.6.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version adds support for provisioning of watsonx services with private endpoints.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.6.0){: external} on GitHub.

### 09 September 2024
{: #subcollection-09sep2024}
{: release-note}

Version 1.5.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.5.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version adds support for `watsonx Orchestrate` deployment.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.5.0){: external} on GitHub.

## August 2024
{: #subcollection-aug2024}

### 03 August 2024
{: #subcollection-03aug2024}
{: release-note}

Version 1.4.2 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.4.2 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version includes bug fixing and dependencies updates.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.4.2){: external} on GitHub.

### 02 August 2024
{: #subcollection-02aug2024}
{: release-note}

Version 1.4.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.4.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version allows referencing existing service instances instead of provisioning new ones.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.4.0){: external} on GitHub.

## July 2024
{: #subcollection-jul2024}

### 10 July 2024
{: #subcollection-10jul2024}
{: release-note}

Version 1.3.6 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.3.6 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version includes bug fixing and dependencies updates.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.3.6){: external} on GitHub.

## June 2024
{: #subcollection-jun2024}

### 21 June 2024
{: #subcollection-21jun2024b}
{: release-note}

Version 1.3.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.3.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version automates the {{site.data.keyword.IBM_notm}} watsonx.data deployment.
For other changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.3.0){: external} on GitHub.

### 21 June 2024
{: #subcollection-21jun2024}
{: release-note}

Version 1.2.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.2.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version extends the deployable locations support for some of the {{site.data.keyword.IBM_notm}} watsonx services to `eu-gb` and `jp-tok`.
For other changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.2.0){: external} on GitHub.

### 10 June 2024
{: #subcollection-10jun2024}
{: release-note}

Version 1.1.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture available
:   Version 1.1.0 of the Watsonx.ai SaaS with Assistant and Governance deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version includes storage delegation feature to encrypt Cloud Object Storage buckets using {{site.data.keyword.IBM_notm}} Key Protect instance.
For other changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.1.0){: external} on GitHub.

## 15 May 2024
{: #subcollection-may2024}
{: release-note}

Introducing Watsonx.ai SaaS with Assistant and Governance deployable architecture : The Watsonx.ai SaaS with Assistant and Governance deployable architecture can be used to create a ready to use {{site.data.keyword.IBM}} watsonx platform in a target {{site.data.keyword.Bluemix_notm}} account. For more information, see [Watsonx.ai SaaS with Assistant and Governance Automation with Assistant and Governance
](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-watsonx-ai-reference-architecture).
