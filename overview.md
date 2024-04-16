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

The Watsonx AI SaaS deployable architecture automates the deployment and setup of
the IBM watsonx platform in an IBM Cloud account.
The IBM watsonx platform is made of several services working together to offer AI capabilities to end users,
who can explore them using [IBM watsonx projects](https://dataplatform.cloud.ibm.com/docs/content/wsj/manage-data/manage-projects.html?context=wx&audience=wdp).
On that purpose, the automation also configures a *starter project* for an existing IBM Cloud user in the target IBM Cloud account.

{: shortdesc}

The deployable architecture can then help setting up an IBM watsonx platform ready to use in one or more Enterprise accounts granting administrator access
to an AI Researcher or any other professional who needs access to advanced AI technologies for their work.

The deployable architecture can also be used as part of a larger solution, where it is included in a stack
of other components.
To facilitate those business challenges, the Watsonx AI SaaS deployable architecture provides output parameters that can be used programmatically
for wiring the deployable architecture to the other components of the stack, and it implements the flexibility
to install additional Watson services.

## Watsonx AI SaaS deployable architecture

The Watsonx AI SaaS deployable architecture performs the following steps to lay down a ready to use IBM watsonx platform
in a target IBM Cloud account, Resource Group, and IBM Cloud Location:

- Creates or use an existing Resource Group in the target IBM Cloud account;
- Creates the following services in the target Resource Group and Location:
  - Cloud Object Storage;
  - Watson Studio;
  - Watson Machine Learning;
- Optionally it can create one or more of the following services in the target Resource Group and Location:
  - watsonx.governance service in the target Resource Group and Location;
  - watsonx Assistant;
  - Watson Discovery;
- It creates the IBM watsonx user profile for an existing user in the target IBM Cloud account (also referred as IBM watsonx admin);
- It creates a starter IBM watsonx project.

As result, the IBM watsonx admin can log into the [IBM watsonx platform](http://dataplatform.cloud.ibm.com/wx/home?context=wx)
and start working with the starter project.

The Watsonx AI SaaS deployable architecture aligns with the [VPC reference architecture for IBM Cloud for Financial Services](https://cloud.ibm.com/docs/framework-financial-services?topic=framework-financial-services-about) security and compliance controls.
