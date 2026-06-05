---

copyright:
  years: 2024
lastupdated: "2024-04-18"

keywords:

subcollection: watsonx-ai-saas-automation

content-type: release-note

---

{{site.data.keyword.attribute-definition-list}}

# Release notes for Cloud foundation for AI ops and governance with watsonx deployable architecture
{: #release-notes}

Use these release notes to learn about the latest updates to Cloud foundation for AI ops and governance with watsonx deployable architecture that are grouped by date. Release notes are available for a minimum of three years.
{: shortdesc}

## June 2026
{: #subcollection-jan2026}

### 05 June 2026
{: #subcollection-05june2026}
{: release-note}

Version 2.3.10 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 2.3.10 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - Updated core modules (`configure_user`, `storage_delegation`, `configure_project`) to reference `terraform-ibm-modules/watsonx-ai/ibm`, with seamless migration of existing resources.
    - Introduced improved KMS handling with a moved block to preserve existing keys and avoid recreation, alongside minor one-time resource transitions that do not impact provisioned services.
    - Added a `.terraformignore` file to exclude symlinks when using terraform stacks.
    - The IBM terraform provider has been updated to support IBM provider v2 (i.e. version > 2.0.0)

## January 2026
{: #subcollection-jan2026}

### 26 January 2026
{: #subcollection-26jan2026}
{: release-note}

Version 2.2.27 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 2.2.27 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - The existing instance related inputs have been updated to a dropdown box in the user interface so it is no longer required to pass full CRN string values.
    - Added update support to the storage delegation api call.
    - Disabled restapi provider debug logging.
    - The IBM terraform provider has been updated to version 1.87.2.

## December 2025
{: #subcollection-dec2025}

### 3 December 2025
{: #subcollection-3dec2025}
{: release-note}

Version 2.1.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 2.1.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - Updated the tile content with a list of features.
    - Improved UI experience for several inputs.
    - The IBM terraform provider has been updated to version 1.85.0.
    - The Mastercard restapi provider has been updated to version 2.0.1.

## November 2025
{: #subcollection-nov2025}

### 4 November 2025
{: #subcollection-4nov2025}
{: release-note}

Version 2.0.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 2.0.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - Solution updated to run on terraform v1.12.2.
    - Added fix for bug which caused an error when using an existing Object Storage instance but allowing the solution to create a new KMS key.

## October 2025
{: #subcollection-oct2025}

### 29 October 2025
{: #subcollection-29oct2025}
{: release-note}

Version 2.0.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 2.0.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    Support has been removed to create a new resource group. The `use_existing_resource_group` and `resource_group_name` inputs have been replace by a single input `existing_resource_group_name`.
    {: important}

    - The following inputs have been renamed:
        - `location` -> `region`
        - `resource_prefix` -> `prefix`
    - `Premium` plan support for Watson Discovery has been removed.
    - `Trial` and `Enterprise with data isolation` plan support for WatsonX Assistant has been removed.
    - The default value of the `cos_kms_new_key_name` has been updated to "wx-saas-da-key".

### 27 October 2025
{: #subcollection-27oct2025}
{: release-note}

Version 1.12.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.12.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - Support added to use an existing Object Storage instance using new input `existing_cos_instance_crn`.
    - Support added for `ca-tor` and `au-syd` regions.
    - Updated the supported input values for `watsonx_orchestrate_plan`.
    - Real time validation has been added to the Projects user interface for inputs.

## September 2025
{: #subcollection-sep2025}

### 8 September 2025
{: #subcollection-8sep2025}
{: release-note}

Version 1.9.38 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.9.38 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - The default value of `enable_cos_kms_encryption` is now false.
    - The IBM terraform provider has been updated to version 1.80.0.
    - Updated all dependant modules to their the latest versions.

## January 2025
{: #subcollection-jan2025}

### 16 January 2025
{: #subcollection-16jan2025}
{: release-note}

Version 1.9.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.9.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} [catalog](/catalog#deployable_architecture){: external}.

    - Fixed bug where incorrect api endpoint was being used for the `eu-gb` region.
    - Update the scope of the KMS auth policy so that it is now scoped to the exact KMS key. Updating to this version from a previous version will see the destroy and recreate of the auh policy, however the new policy will be created before the old one so there will be no disruption to every day serivces during upgrade.
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

Version 1.6.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.6.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version adds support for provisioning of watsonx services with private endpoints.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.6.0){: external} on GitHub.

### 09 September 2024
{: #subcollection-09sep2024}
{: release-note}

Version 1.5.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.5.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version adds support for `watsonx Orchestrate` deployment.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.5.0){: external} on GitHub.

## August 2024
{: #subcollection-aug2024}

### 03 August 2024
{: #subcollection-03aug2024}
{: release-note}

Version 1.4.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.4.2 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version includes bug fixing and dependencies updates.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.4.2){: external} on GitHub.

### 02 August 2024
{: #subcollection-02aug2024}
{: release-note}

Version 1.4.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.4.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version allows referencing existing service instances instead of provisioning new ones.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.4.0){: external} on GitHub.

## July 2024
{: #subcollection-jul2024}

### 10 July 2024
{: #subcollection-10jul2024}
{: release-note}

Version 1.3.6 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.3.6 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version includes bug fixing and dependencies updates.
For the complete list of changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.3.6){: external} on GitHub.

## June 2024
{: #subcollection-jun2024}

### 21 June 2024
{: #subcollection-21jun2024b}
{: release-note}

Version 1.3.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.3.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version automates the {{site.data.keyword.IBM_notm}} watsonx.data deployment.
For other changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.3.0){: external} on GitHub.

### 21 June 2024
{: #subcollection-21jun2024}
{: release-note}

Version 1.2.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.2.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version extends the deployable locations support for some of the {{site.data.keyword.IBM_notm}} watsonx services to `eu-gb` and `jp-tok`.
For other changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.2.0){: external} on GitHub.

### 10 June 2024
{: #subcollection-10jun2024}
{: release-note}

Version 1.1.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture available
:   Version 1.1.0 of the Cloud foundation for AI ops and governance with watsonx deployable architecture is available in the {{site.data.keyword.cloud_notm}} catalog. This version includes storage delegation feature to encrypt Cloud Object Storage buckets using {{site.data.keyword.IBM_notm}} Key Protect instance.
For other changes in the release, see the [release notes](https://github.com/terraform-ibm-modules/terraform-ibm-watsonx-saas-da/releases/tag/v1.1.0){: external} on GitHub.

## 15 May 2024
{: #subcollection-may2024}
{: release-note}

Introducing Cloud foundation for AI ops and governance with watsonx deployable architecture : The Cloud foundation for AI ops and governance with watsonx deployable architecture can be used to create a ready to use {{site.data.keyword.IBM}} watsonx platform in a target {{site.data.keyword.Bluemix_notm}} account. For more information, see [Cloud foundation for AI ops and governance with watsonx Automation with Assistant and Governance
](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-watsonx-ai-reference-architecture).
