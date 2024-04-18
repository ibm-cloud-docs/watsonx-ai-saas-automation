---

copyright:
  years: 2024
lastupdated: "2024-04-16"

keywords: question about Watsonx AI SaaS

subcollection: watsonx-ai-saas-automation

content-type: troubleshoot

---

<!-- keywords values above are place holders. Actual values should be pulled from the Troubleshooting questions or error message to which the issue relates. Only use a messageID if the troubleshooting topic is about an issue encountered from an error message that has an ID.  -->

{{site.data.keyword.attribute-definition-list}}

<!-- You must add the troubleshoot content type in your attribute definitions AND on a new line under each troubleshooting topic H1 ID. This will ensure that the troubleshooting entry is pulled into other locations, like chatbots. Use the support attribute definition for reuse in the support center. For more information, see  https://test.cloud.ibm.com/docs/writing?topic=writing-support-center#support-center-troubleshoot-->

<!-- Remember that this is the individual topic template for each troubleshooting entry that belongs in a troubleshooting topic group in the Help left nav group. For more information, see the guidance page: https://test.cloud.ibm.com/docs/writing?topic=writing-troubleshooting-topics-->

# Watsonx AI SaaS deployment failed, how do I proceed?
{: #troubleshoot-deploy}
{: troubleshoot}

Your deployment failed.
{: shortdesc}

You attempted to deploy the Watsonx AI SaaS deployable architecture in an IBM Cloud account, but it failed.
{: tsSymptoms}

The Watsonx AI SaaS installs several IBM Cloud services and performs several configuration tasks during the deployment.
An issue in one of those tasks is causing the failure. For example a lack of authorization in installing one of the services.
{: tsCauses}

If the deployment process does not finish successfully, look at the IBM Cloud projects configuration logs.
These logs typically provide the information about the component that causes the issue.

If you can't deploy successfully, follow these steps:

1.  Make sure that you comply with the prerequisites in the [planning](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-planning)) topic.
2.  Check the values of the inputs.

    From the **Configurations** tab in your project, click the name of your deployable architecture > **Edit**. Review the input parameters and
    save the configuration.
3.  Validate the configuration changes, and rerun the deploy.

If the issue persists, [open a case](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-help-and-support) in the {{site.data.keyword.cloud_notm}} support center.
{: tsResolve}
