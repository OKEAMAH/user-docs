# Application context for SCM Integrations

{% hint style="warning" %}
Release status

All the Application context integrations listed on this page are in Early Access and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro.
{% endhint %}

These are the available integrations that you can set up for the application context:

* [Backstage file](./#backstage-file-for-scm-integrations)&#x20;
* [ServiceNow CMDB](./#servicenow-cmdb-for-scm-integrations)
* [Atlassian Compass](./#atlassian-compass)
* [Harness](./#harness)
* [OpsLevel](./#opslevel)
* [Datadog Service Catalog](./#datadog-service-catalog) &#x20;

{% hint style="info" %}
The Application Context integrations on this page work in conjunction with assets found through AppRisk SCM integrations. If there is no Snyk AppRisk SCM integration configured at the Group level on the Integrations page, then data will not populate from these integrations.
{% endhint %}

## Backstage file for SCM integrations

{% hint style="warning" %}
**Release status**

The Backstage file integration is in [Early Access](https://docs.snyk.io/getting-started/snyk-release-process#early-access) and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro plans.
{% endhint %}

Backstage is a service catalog that allows users to add metadata or annotations to their repositories, helping to organize and categorize the available resources for easier navigation and understanding. You can leverage your SCM integration to pull metadata associated with Backstage catalog files into Snyk AppRisk.

You can use the Backstage catalog file for GitHub, GitLab, Azure DevOps, BitBucket Cloud, and BitBucket on-prem SCM integrations.

### Required Parameters for Backstage file

* A configured SCM integration.&#x20;
* The `catalog-info.yaml` file from your Project.

### Integration Hub setup for Backstage file

1. Open the **Integration Hub** menu.&#x20;
2. Select an SCM integration.&#x20;
3. Click the **Settings** option of the SCM integration.&#x20;
4. Enable the **Add Backstage Catalog** option.
5. Optional - if the Backstage catalog filename in your repository is not `catalog-info.yaml` you can change the default value in the Backstage catalog filename field.
6. Select at least one attribute you want to add to Snyk AppRisk.

{% hint style="info" %}
Snyk AppRisk parses the fields of the detected file using the default field names unless an alternate field name is specified.
{% endhint %}

7. Click the **Done** button.

After you finish configuring the Backstage catalog, Snyk AppRisk starts enriching your repository assets with the data found in the backstage catalog .yaml file.

{% hint style="warning" %}
When you set up the catalog attributes, you must use the specific service-level attributes, for example `attribute.name.`
{% endhint %}

## ServiceNow CMDB for SCM integrations

{% hint style="warning" %}
**Release status**

The ServiceNow CMDB integration is in [Early Access](https://docs.snyk.io/getting-started/snyk-release-process#early-access) and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro plans.
{% endhint %}

### Required Parameters for ServiceNow CMDB <a href="#servicenow-cmdb-required-parameters" id="servicenow-cmdb-required-parameters"></a>

1. Add the **profile name** for your ServiceNow CMDB instance.
2. Setup the **CMDB instance** for the ServiceNow CMDB by following this example `https://<INSTANCE_NAME>.service-now.com`.
3. **Username** and **Password** - Credentials for your ServiceNow CMDB instance.
4. Add the t**able name** for the CMDB configuration item class. Navigate to the [ServiceNow CMDB tables details](https://docs.servicenow.com/bundle/washingtondc-servicenow-platform/page/product/configuration-management/reference/cmdb-tables-details.html) page for the full list of names.&#x20;
5. Add the **CMDB field to map Repo URL** - Add the URL of the repository.

{% hint style="info" %}
* The data gathered by Snyk from ServiceNow CMDB will be correlated with the Repository Assets.
* The ServiceNow CMDB integration uses basic authentication and suggests enabling the "Web service access only" option for Service Accounts.&#x20;
{% endhint %}

### Integration Hub setup for ServiceNow CMDB <a href="#servicenow-cmdb-integration-hub-setup" id="servicenow-cmdb-integration-hub-setup"></a>

* Open the **Integration Hub** menu.&#x20;
* Select the **App Context** tag and search for ServiceNow CMDB.&#x20;
* Click the **Add** button.
* Add the **Profile name** - this is the name of your ServiceNow CMDB profile.
* Add the **CMDB Instance** - this is your ServiceNow instance, use this format: `https://<INSTANCE_NAME>.service-now.com`
* Add the **Username** and the **Password**- the username and password to access the ServiceNow CMDB instance
* Add the **Table name** - select the configuration item class that Snyk AppRisk should onboard. Use this format `cmdb_ci_<class>`
* Add the **CMDB Field to map Repo URL** - the specific URL that is being referred to in the ServiceNow CMDB record.
* You can select one or more attributes related to repository assets and configure where Snyk AppRisk can take this attribute in ServiceNow CMDB. Example:&#x20;
  * Category: application\_type
  * Owner: business\_unit
* Click the **Done** button.
* When the connection is established, the status of the ServiceNow CMDB integration is changed to **Connected**.

{% hint style="warning" %}
When you set up the catalog attributes, you can customize the name of the attribute but must ensure that the same name is used in the catalog and in the Integration Hub setup.
{% endhint %}

The following video provides an overview of the ServiceNow CMDB option from the Integration Hub and a quick explanation of the available attributes:

{% embed url="https://youtu.be/I4EyhOeQGT0" %}
Liked the video? Checkout the rest of the course on [Snyk Learn](https://learn.snyk.io/catalog/?type=product-training\&topics=AppRisk)!
{% endembed %}

## Atlassian Compass

{% hint style="warning" %}
**Release status**

The Atlassian Compass integration is in [Early Access](https://docs.snyk.io/getting-started/snyk-release-process#early-access) and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro plans.
{% endhint %}

### Required Parameters for Atlassian Compass

1. Add your Atlassian Compass **Profile name**.
2. Add your Atlassian Compass **Instance URL**. You can use this format type: `https://<YOUR ORGANIZATION>.atlassian.net`.
3. Add your Atlassian Compass **Username**.
4. Add your Atlassian Compass instance **Token**. Navigate to the [Manage API tokens for your Atlassian account](https://support.atlassian.com/atlassian-account/docs/manage-api-tokens-for-your-atlassian-account/) page for more details about creating an Atlassian API token. &#x20;

{% hint style="info" %}
The gathered data from Atlassian Compass will be correlated with the Repository Assets.

This feature is available only for the integration with Atlassian Compass.
{% endhint %}

### Integration Hub setup for Atlassian Compass

1. Open the **Integration Hub** menu.&#x20;
2. Select the **App Context** tag and search for Atlassian Compass.&#x20;
3. Click the **Add** button.
4. Add the **Profile name** - this is the name of your Atlassian Compass profile.
5. Add the **Instance URL** - this is the URL of the Atlassian Compass instance. Use this format type: `https://<YOUR ORGANIZATION>.atlassian.net`
6. Add the **Username** - this is the username to access the Atlassian Compass instance.
7. Add the **Token** - this is the API token to access the Atlassian Compass instance.&#x20;
8. You can select one or more attributes related to repository assets that Snyk AppRisk can pull from Atlassian Compass based on the [Component Data](https://developer.atlassian.com/cloud/compass/forge-graphql-toolkit/Interfaces/Component/):&#x20;
   * **Catalog Name** - Matches with name.
   * **Category** - Identified when '`fields.definition.name`' equals tier.
   * **Lifecycle** - Identified when '`fields.definition.name`' equals lifecycle.
   * **Owner** - the `ownerId` (finding owner name from ownerId).
   * **Application** - the `typeId` (all component types, Application, Service, Library, and so on receive an ID).
9. Click the **Done** button.
10. When the connection is established, the status of the Atlassian Compass integration is changed to **Connected**, and Snyk AppRisk will start enriching repository assets with the data found in Atlassian Compass.

{% hint style="warning" %}
When you set up the catalog attributes, you must use the specific service-level attributes, for example `attribute.name.`
{% endhint %}

## Harness

{% hint style="warning" %}
**Release status**

The Harness integration is in [Early Access](https://docs.snyk.io/getting-started/snyk-release-process#early-access) and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro plans.
{% endhint %}

### Required Parameters for Harness

1. Add your Harness **Profile name**.
2. Add the **Host URL** of your Harness account. You can use this format type: `https://<YOUR ORGANIZATION>.harness.io`
3. Add the **API key** for your Harness instance. You can use the Harness [Add and manage your API keys](https://developer.harness.io/docs/platform/automation/api/add-and-manage-api-keys/) documentation page to manage your API key.

{% hint style="info" %}
This integration is focused on [Harness’s](https://developer.harness.io/docs/internal-developer-portal/catalog/software-catalog/) service catalog module and it is backed by the Backstage catalog.
{% endhint %}

### Integration Hub setup for Harness

1. Open the **Integration Hub** menu.&#x20;
2. Select the **App Context** tag and search for Harness.&#x20;
3. Click the **Add** button.
4. Add the **Profile name** - this is the name of your Harness instance.
5. Add the **Host URL** of your Harness account.&#x20;
6. Add the **API key** of your Harness instance.
7. Select at least one Harness software catalog [metadata](https://developer.harness.io/docs/internal-developer-portal/catalog/software-catalog#component-definition-yaml):
   * Catalog name - If you select this metadata, it is mandatory to add the **Catalog name key**.
   * Title - If you select this metadata, it is mandatory to add the **Title key**.
   * Category - If you select this metadata, it is mandatory to add the **Category key**.
   * Lifecycle - If you select this metadata, it is mandatory to add the **Lifecycle key**.
   * Owner - If you select this metadata, it is mandatory to add the **Owner key**.
   * Application - If you select this metadata, it is mandatory to add the **Application key**.
8. Click the **Done** button.
9. When the connection is established, the status of the Harness integration is changed to **Connected**, and Snyk AppRisk will start enriching repository assets with the data found in Harness.

{% hint style="warning" %}
When you set up the catalog attributes, you can customize the name of the attribute but must ensure that the same name is used in the catalog and in the Integration Hub setup.
{% endhint %}

## OpsLevel

{% hint style="warning" %}
**Release status**

The OpsLevel integration is in [Early Access](https://docs.snyk.io/getting-started/snyk-release-process#early-access) and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro plans.
{% endhint %}

### Required Parameters for OpsLevel

1. Add your OpsLevel **Profile name**.
2. Add the **Instance URL** of your OpsLevel account. You can use this format type: `https://<YOUR Organizer>.opslevel.com`
3. Add the **API Token** for your OpsLevel instance. To create an API Token in your OpsLevel account, use the instructions on the OpsLevel [Create an API token](https://docs.opslevel.com/docs/graphql#1-create-an-api-token) documentation page.

### Integration Hub setup for OpsLevel

1. Open the **Integration Hub** menu.&#x20;
2. Select the **App Context** tag and search for OpsLevel.&#x20;
3. Click the **Add** button.
4. Add the **Profile name** - this is the name of your OpsLevel instance.
5. Add the **Instance URL** of your OpsLevel account.&#x20;
6. Add the **API Token** for your OpsLevel instance.
7. You can select one or more attributes related to repository assets that Snyk AppRisk can pull from OpsLevel with the following mapping:
   * Catalog name - Identified with `name` in OpsLevel.
   * Category - Identified with `tier.name` in OpsLevel.
   * Lifecycle - Identified with `lifecycle.name` in OpsLevel.
   * Owner - Identified with `owner.name` in OpsLevel.
   * Application - Identified with `product` in OpsLevel.
8. Click the **Done** button.
9. When the connection is established, the status of the OpsLevel integration is changed to **Connected**, and Snyk AppRisk will start enriching repository assets with the data found in OpsLevel.

{% hint style="warning" %}
When you set up the catalog attributes, you must use the specific service-level attributes, for example `attribute.name.`
{% endhint %}

## Datadog Service Catalog

{% hint style="warning" %}
**Release status**

The Datadog Service Catalog integration is in [Early Access](https://docs.snyk.io/getting-started/snyk-release-process#early-access) and available for both Snyk AppRisk Essentials and Snyk AppRisk Pro plans.
{% endhint %}

### Required Parameters for Datadog Service Catalog

1. Add your Datadog **Profile name**.
2. Add the **API key** for the Datadog instance. Your token should have the following scope permissions: `apm_service_catalog_read`.
3. Add the **Application Key** along with your organization's API key to grant users access to Datadog's programmatic API. For more details, access the [Datadog API and Application key](https://docs.datadoghq.com/account\_management/api-app-keys/) documentation page.

### Integration Hub setup for Datadog Service Catalog

1. Open the **Integration Hub** menu.&#x20;
2. Select the **App Context** tag and search for **Datadog Service Catalog**.&#x20;
3. Click the **Add** button.
4. Add the **Profile name** - this is the name of your Datadog instance.
5. Add the **API key** for your Datadog instance.
6. Add the **Application key** for your Datadog instance.
7. Add the details of your **Datadog site**.
8. You can select one or more attributes related to repository assets that Snyk AppRisk can pull from Datadog Service Catalog with the following mapping:
   * Catalog name - If you select this metadata, it is mandatory to add the **Catalog name key**.
   * Title - If you select this metadata, it is mandatory to add the **Title key**.
   * Category - If you select this metadata, it is mandatory to add the **Category key**.
   * Lifecycle - If you select this metadata, it is mandatory to add the **Lifecycle key**.
   * Owner - If you select this metadata, it is mandatory to add the **Owner key**.
   * Application - If you select this metadata, it is mandatory to add the **Application key**.
9. Click the **Done** button.
10. When the connection is established, the status of the Datadog Service Catalog integration is changed to **Connected**, and Snyk AppRisk will start enriching repository assets collected by a Snyk AppRisk SCM Integration with the data found in Datadog Service Catalog.

{% hint style="warning" %}
When you set up the catalog attributes, you can customize the name of the attribute but must ensure that the same name is used in the catalog and in the Integration Hub setup.
{% endhint %}

\
