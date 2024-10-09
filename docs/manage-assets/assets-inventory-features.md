# Assets inventory features

{% hint style="warning" %}
**Release status** \
**Risk factors** on assets, **Runtime discovered** and **Runtime last seen** filters are currently in Closed Beta and available only with Snyk AppRisk Pro.&#x20;
{% endhint %}

Snyk AppRisk provides powerful search and filtering capabilities to help you narrow in on assets for investigation and mitigation.

## Search capabilities

Use the search bar to search for specific keywords across various asset properties. Results can also include data retrieved from the Attributes tab of an asset, not only by the asset name.&#x20;

## Filters capabilities

### Quick filters

Quick filters are pre-defined filters to help you quickly focus on important assets. Here are the available quick filters:

* Assets with risk factors `Deployed` and `Public facing` and `No Coverage`: displays only the assets that have both the `Deployed` and `Public facing` risk factors available, and with a coverage gap on any of the selected Snyk products (available in Snyk AppRisk Pro only).
* Assets with risk factor `Deployed` and `No Coverage`: displays only the assets that have both the `Deployed` risk factor available, and with a coverage gap on any of the selected Snyk products  (available in Snyk AppRisk Pro only).
* Assets with Repository freshness Active and No Coverage: displays only the assets from active repositories and with a coverage gap on any of the selected Snyk products.
* Assets with `Asset Class A` and `No Coverage:`displays only the assets that are Class A and with a coverage gap on any of the selected Snyk products.

{% hint style="info" %}
After applying a quick filter, you can change or add additional filters by clicking on **Advanced Filters**.&#x20;
{% endhint %}

If you had a quick filter selected and then added an advanced filter, the quick filter will be deselected. In the **Advanced Filters** section, you can see the filters used to create the **Quick filter** you selected and can add additional filters on top of those. &#x20;

### Advanced filters

With this feature, you can [define filters](../manage-risk/policies/assets-policies/create-policies.md#define-filters) and filter assets based on highly specific criteria. For example, repository assets that have `AWS` in the name, are classified as either **A** or **B**, and do not have Snyk IaC as a control executed. This can be useful for finding repositories that have infrastructure as code that Snyk IaC is not currently scanning.

Click Filters from the top left side of the screen. A pop-up is displayed allowing you to add quick filters or advanced filters.  If you select the Advanced filters, you can specify one or more sets of criteria as follows:

* **Property** of an asset (such as asset name, class, control executed).
* **Condition** depends on the asset selected (such as `contains` or `does not contain` for `asset name`).
* **Value** depends on the Property and Condition.

You can add as many filters as needed. To add another filter click **Add Filter,** set the condition as **And** or **Or** and customize the **Property**, **Condition**, and **Value** fields.&#x20;

{% hint style="info" %}
If you use Snyk AppRisk for the first time, start with the **Coverage** filter to determine where you currently have Snyk Implemented.
{% endhint %}

You can filter the information for all the inventory layouts and can use the following filters available under the **Advanced filters** section:

* **Application\*** - the list of the applications for which you have configured the application context catalog in Snyk AppRisk.
* **Asset ID** - the unique identifier of the asset.
* **Asset name** - the name of the asset.
* **Asset type** - repository, package, or scanned artifact.
* **Attribute** - asset attributes retrieved from the data source.
* **Catalog name\*** - the name of your application context catalog.
* **Category**\* - the category of a repository asset. For example, service or library.
* **Class** - specify the class of the asset.
* **Coverage** - specify the product or products used to scan the asset. The Coverage filter identifies if at least one scan has been run by the specified product.
* **Coverage gap** - specify the products for which the asset has not been scanned and do not meet the Set Coverage Control Policy requirements. The coverage gap applies only if you previously defined the coverage requirements of an asset and the asset has never been scanned, or the last scan is older than the default scanning frequency.
* **Developers** - specify the developer or developers who contributed to the asset.
* **Discovered** - specify the period when the asset was discovered.
* **Issue severity** - specify the severity of the issue: critical, high, medium, low.
* **Issue source** - specify where the issue was identified: SCM or third-party integrations. A source category will only be visible if there is at least one source present.
* **Last seen** - specifies the most recent time this asset was detected by Snyk in any of the sources (for example, Snyk, SCM, and so on).
* **Lifecycle\*** - represents the lifecycle state of the application context catalog component, for example `production`, `experimental`, `deprecated`.
* **Locked attributes** - specify if the attribute value is locked.
* **Owner\*** - represents the team owning the repository for which the application context catalog was configured.
* **Risk factors** - The list of available risk factors. Risk factors refer to assets that can be vulnerable to security threats based on their exposure, sensitivity, compliance with security standards, and vulnerability history.
* **Runtime discovered** - specify the period when the runtime image asset was discovered.
* **Runtime last seen** - specifies the most recent time this image asset was detected in runtime
* **SCM Repository freshness** - the status of the repository and the date of the last commit.
  * **Active**: Had commits in the last 3 months.
  * **Inactive**: The last commits were made in the last 3 - 6 months.
  * **Dormant**: No commits in the last 6 months.
  * **N/A**: There are no commits detected by Snyk AppRisk.
* **Source** - specify the asset source.
* **Tags** - information about the detected languages and repository update status.
* **Title\*** - represents the name of the component for which the application context catalog was configured.

**\***All filters marked with `*` are visible only to the users who configured the [application context](../scm-ide-and-ci-cd-integrations/snyk-scm-integrations/application-context-for-scm-integrations/) catalog for their SCM integrations.

After applying the filters, the asset list will display only the assets that match the specified conditions, without a hierarchical structure.

{% hint style="info" %}
**Coverage** and **Coverage gap**  filter differences

* Use the Coverage filter to identify the assets scanned by the products at least once.
* Use the Coverage gap filter for assets that do not meet the requirements defined in the Set coverage control policy.&#x20;

The Coverage gap filter identifies assets that fall 'out of policy' and do not satisfy the coverage criteria you have specified, due to infrequent scanning or no scanning at all. On the other hand, the Coverage filter allows you to locate assets that have or have not been scanned, irrespective of any coverage requirements.
{% endhint %}



