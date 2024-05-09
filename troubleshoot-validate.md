---

copyright:
  years: 2024
lastupdated: "2024-04-30"

keywords: question about Watsonx AI SaaS

subcollection: watsonx-ai-saas-automation

content-type: troubleshoot

---

<!-- keywords values above are place holders. Actual values should be pulled from the Troubleshooting questions or error message to which the issue relates. Only use a messageID if the troubleshooting topic is about an issue encountered from an error message that has an ID.  -->

{{site.data.keyword.attribute-definition-list}}

<!-- You must add the troubleshoot content type in your attribute definitions AND on a new line under each troubleshooting topic H1 ID. This will ensure that the troubleshooting entry is pulled into other locations, like chatbots. Use the support attribute definition for reuse in the support center. For more information, see  https://test.cloud.ibm.com/docs/writing?topic=writing-support-center#support-center-troubleshoot-->

<!-- Remember that this is the individual topic template for each troubleshooting entry that belongs in a troubleshooting topic group in the Help left nav group. For more information, see the guidance page: https://test.cloud.ibm.com/docs/writing?topic=writing-troubleshooting-topics-->

# Why did the Watsonx AI SaaS validation fail?
{: #troubleshoot-validate}
{: troubleshoot}

You must have a successful Watsonx AI SaaS deployable architecture validation.
{: shortdesc}

The validation of a Watsonx AI SaaS deployable architecture for IBM Cloud projects configuration failed.
{: tsSymptoms}

The Watsonx AI SaaS requires setting several input parameters during the configuration phase. The most common reason for failures during the validation is because of a bad value set for some of those parameters.
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
