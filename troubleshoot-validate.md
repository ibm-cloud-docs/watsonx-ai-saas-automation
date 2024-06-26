---

copyright:
  years: 2024
lastupdated: "2024-05-13"

keywords: question about Watsonx.ai SaaS with Assistant and Governance

subcollection: watsonx-ai-saas-automation

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why did the Watsonx.ai SaaS with Assistant and Governance validation fail?
{: #troubleshoot-validate}
{: troubleshoot}

You must have a successful Watsonx.ai SaaS with Assistant and Governance deployable architecture validation.
{: shortdesc}

The validation of a Watsonx.ai SaaS with Assistant and Governance deployable architecture for {{site.data.keyword.Bluemix_notm}} projects configuration failed.
{: tsSymptoms}

The Watsonx.ai SaaS with Assistant and Governance requires setting several input parameters during the configuration phase. The most common reason for failures during the validation is because of a bad value set for some of those parameters.
{: tsCauses}

If the validation process does not finish successfully, look at the {{site.data.keyword.Bluemix_notm}} projects configuration logs.
These logs typically provide the information about the root cause of the issue.

If you can't validate successfully, follow these steps:

1.  Make sure that you completed the prerequisites in the [planning](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-planning) topic.
2.  Check the values of the inputs.
      1. From the **Configurations** tab in your project, click the name of your deployable architecture.
      2. Click **Edit**. Review the input parameters.
      3. Save the configuration.
3.  Validate the configuration changes again.

If the issue continues, [open a case](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-help-and-support) in the {{site.data.keyword.cloud_notm}} support center.
{: tsResolve}
