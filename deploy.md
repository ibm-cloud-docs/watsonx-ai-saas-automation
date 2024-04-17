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

You can deploy a deployable architecture from the {{site.data.keyword.cloud_notm}} catalog. You can choose among different deployment options, including with {{site.data.keyword.cloud_notm}} projects. [Learn about IaC deployments with projects](/docs/secure-enterprise?topic=secure-enterprise-understanding-projects).

## Deploying with {{site.data.keyword.cloud_notm}} projects
{: #watsonx-ai-saas-deploy-cloud}

To deploy the Watsonx AI SaaS deployable architecture through the {{site.data.keyword.cloud_notm}} catalog, follow these steps:

1.  Make sure that you comply with the prerequisites in the [planning](/docs/watsonx-ai-saas-automation?topic=watsonx-ai-saas-automation-planning) topic:
    - Have configured the IBM Cloud target account.
    - Have configured IBM Cloud projects to deploy in the target account.
    - Have defined and verified the access roles.
2.  Go to the {{site.data.keyword.cloud_notm}} [catalog](/catalog#reference_architecture){: external} and search for Watsonx AI SaaS.
3.  Click the tile for the deployable architecture to open the details.
4.  Select the latest product version in the Architecture section.
5.  Select a variation, if more than one is available.
6.  Click **Add to project**.
    1.  Name your project, enter a description, and specify a configuration name. Click **Create**.
    2.  Select the region and the resource group where project artifacts must be stored.
7.  Edit and validate the configuration:
    1.  Select your authentication method. You can use a Trusted profile or an existing secret in {{site.data.keyword.secrets-manager_short}}. Alternatively, you can add your API key directly, which is not recommended. For more information, see [Using an API key or secret to authorize projects](/docs/secure-enterprise?topic=secure-enterprise-authorize-project).
    2.  Enter the name of the target resource group from the Required tab.
    3.  From the Optional tab select a value or leave the default for:
        1.  the target location for the servies being deployed.
        2.  the service plan for the required services.
        3.  the service plan for the optional services (default is `do not install`).
        4.  whether the target resource group exists already, or it must be created.
    4.  From the Optional tab enter a value or accept the default for:
        1.  the resource prefix for uniquely naming the services being provisioned.
        2.  the IBM watsonx admin api key. It is recommended to store in advance the api key in the Secrets Manager integrated
            with the IBM Cloud projects and reference it from there.
        3.  the name of the IBM Watsonx starter project.
    5.  Save the configuration.
    6.  Click **Validate**. Validation takes a few minutes.

        {{site.data.keyword.cloud_notm}} projects runs an SCC scan against the IBM Cloud for Financal Services profile. Controls that are part of the deployable architecture and that are also supported by {{site.data.keyword.cloud_notm}} projects are checked. Any extra controls that are not included in the list of supported {{site.data.keyword.compliance_short}} rules are not checked when you validate the configuration.

8.  Deploy the configuration:

    After you validate your configuration, you can deploy it to your target account.

    1.  Review the input values and make any necessary changes.
    2.  Click **Deploy**.

        Deploying the deployable architecture can take a few minutes. You are notified when the deployment is successful.

9.  Review the outputs from the deployable architecture.

During the validation and deployment process, monitor the [needs attention items](/docs/secure-enterprise?topic=secure-enterprise-needs-attention-projects). The widget reflects any issue that occurs in your configurations.
{: remember}
