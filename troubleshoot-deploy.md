---

copyright:
  years: 2024
lastupdated: "2024-04-16"

keywords: question about Watsonx AI SaaS

subcollection: watsonx-ai-saas-automation

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why did the Watsonx AI SaaS deployment fail?
{: #troubleshoot-deploy}
{: troubleshoot}

To successfully deploy the Watsonx AI SaaS deployable architecture, ensure that all the required steps are complete.
{: shortdesc}

You attempted to deploy the Watsonx AI SaaS deployable architecture in an {{site.data.keyword.Bluemix_notm}} account, but it failed.
{: tsSymptoms}

The Watsonx AI SaaS installs several {{site.data.keyword.Bluemix_notm}} services and performs several configuration tasks during the deployment.
An issue in one of those tasks is causing the failure. For example, a lack of authorization in installing one of the services.
{: tsCauses}

If the deployment process does not finish successfully, look at the {{site.data.keyword.Bluemix_notm}} projects configuration logs.
These logs typically provide the information about the component that causes the issue.

If you can't deploy successfully, follow these steps:

1.  Make sure that you completed the prerequisites in the [planning](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-planning) topic.
2.  Check the values of the inputs.
    1. From the **Configurations** tab in your project, click the name of your deployable architecture.
    2. Click **Edit** and review the input parameters.
    3. Save the configuration.
3.  Validate the configuration changes, and rerun the deployment.

If the issue continues, [open a case](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-help-and-support) in the {{site.data.keyword.cloud_notm}} support center.
{: tsResolve}
