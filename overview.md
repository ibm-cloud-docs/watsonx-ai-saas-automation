---

copyright:
  years: 2024
lastupdated: "2024-04-16"

keywords:

subcollection: watsonx-ai-saas-automation

---


{{site.data.keyword.attribute-definition-list}}

# Overview
{: #overview}

The Watsonx AI SaaS deployable architecture automates the deployment and setup of the {{site.data.keyword.IBM}} watsonx platform in an {{site.data.keyword.Bluemix_notm}} account. The {{site.data.keyword.IBM_notm}} watsonx platform is made of several services working together to offer AI capabilities to end users, who can explore them using [IBM watsonx projects](https://dataplatform.cloud.ibm.com/docs/content/wsj/manage-data/manage-projects.html?context=wx&audience=wdp). The automation also configures a starter project for an existing {{site.data.keyword.Bluemix_notm}} user in the target {{site.data.keyword.Bluemix_notm}} account. 
{: shortdesc}

The deployable architecture can help set up an {{site.data.keyword.IBM_notm}} watsonx platform that's ready to use in one or more Enterprise accounts. It grants administrator access to an AI Researcher or any other professional who needs access to advanced AI technologies for their work.

The deployable architecture can also be used as part of a larger solution, where it is included in a stack of other components. To facilitate those business challenges, the Watsonx AI SaaS deployable architecture provides output parameters that can be used programmatically for wiring the deployable architecture to the other components of the stack, and it implements the flexibility to install additional Watson services.

## Watsonx AI SaaS deployable architecture
{: #watsonx-ai-saas-refarch}

The Watsonx AI SaaS deployable architecture performs the following steps to create a ready to use {{site.data.keyword.IBM_notm}} watsonx platform in a target {{site.data.keyword.Bluemix_notm}} account, resource group, and {{site.data.keyword.Bluemix_notm}} location:

- Creates or use an existing resource group in the target {{site.data.keyword.Bluemix_notm}} account
- Creates the following services in the target resource group and location:
  - Cloud Object Storage
  - Watson Studio
  - Watson Machine Learning
- Optionally, it can create one or more of the following services in the target resource group and location:
  - watsonx.governance service in the target resource group and location
  - watsonx Assistant
  - Watson Discovery
- It creates the {{site.data.keyword.IBM_notm}} watsonx user profile for an existing user in the target {{site.data.keyword.Bluemix_notm}} account. This user is also referred as {{site.data.keyword.IBM_notm}}watsonx admin.
- It creates a starter {{site.data.keyword.IBM_notm}} watsonx project.

As result, the {{site.data.keyword.IBM_notm}} watsonx admin can log into the [{{site.data.keyword.IBM_notm}} watsonx platform](http://dataplatform.cloud.ibm.com/wx/home?context=wx) and start working with the starter project.

The Watsonx AI SaaS deployable architecture aligns with the [VPC reference architecture for IBM Cloud for Financial Services](/docs/framework-financial-services?topic=framework-financial-services-about) security and compliance controls.
