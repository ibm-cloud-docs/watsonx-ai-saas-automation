---

copyright:
  years: 2024
lastupdated: "2024-04-16"

keywords:

subcollection: watsonx-ai-saas-automation

---


{{site.data.keyword.attribute-definition-list}}

# Deploying Watsonx AI SaaS deployable architecture
{: #deploy}

You can deploy a deployable architecture from the {{site.data.keyword.cloud_notm}} catalog. You can choose from different deployment options, including an option to deploy with {{site.data.keyword.cloud_notm}} projects. For more information, see [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

## Deploying with {{site.data.keyword.cloud_notm}} projects
{: #deploy-cloud}

To deploy the Watsonx AI SaaS deployable architecture through the {{site.data.keyword.cloud_notm}} catalog, complete the following steps:

1.  Edit and validate the configuration:
    1.  Select your authentication method. You can use a trusted profile or an existing secret in {{site.data.keyword.secrets-manager_short}}. Alternatively, you can add your API key directly, which is not recommended. For more information, see [Using an API key or secret to authorize projects](/docs/secure-enterprise?topic=secure-enterprise-authorize-project).
    1.  Enter the name of the target resource group from the Required tab.
    1.  From the Optional tab, select a value or keep the default for the following options:
        1.  The target location for the servies being deployed.
        2.  The service plan for the required services.
        3.  The service plan for the optional services. The default is "do not install".
        4.  Whether the target resource group exists already, or it must be created.
    1.  From the Optional tab, enter a value or accept the default for the following options:
        1.  The resource prefix for uniquely naming the services that are being provisioned.
        2.  The {{site.data.keyword.IBM_notm}} watsonx admin api key. It is recommended to store the api key in advance in Secrets Manager that's integrated with the {{site.data.keyword.cloud_notm}} projects and reference it from there.
        3.  The name of the {{site.data.keyword.IBM_notm}} Watsonx starter project.
    1.  Save the configuration.
    1.  Click **Validate**. Validation takes a few minutes.

        {{site.data.keyword.cloud_notm}} projects runs an SCC scan against the {{site.data.keyword.cloud_notm}} for Financal Services profile. Controls that are part of the deployable architecture and that are also supported by {{site.data.keyword.cloud_notm}} projects are checked. Any extra controls that are not included in the list of supported {{site.data.keyword.compliance_short}} rules are not checked when you validate the configuration.
{: important}

1.  Deploy the configuration. After you validate your configuration, you can deploy it to your target account:

    1.  Review the input values and make any necessary changes.
    1.  Click **Deploy**. Deploying the deployable architecture can take a few minutes. You are notified when the deployment is successful.

1.  Review the outputs from the deployable architecture.

During the validation and deployment process, monitor the [needs attention items](/docs/secure-enterprise?topic=secure-enterprise-needs-attention-projects). The widget reflects any issue that occurs in your configurations.
{: remember}
