# Analytics

Analytics provides executives, as well as Application Security (AppSec) leaders and practitioners a view into the performance of their AppSec program. Snyk customers can understand at a glance the strengths and weaknesses of their program, identify where successful practices can be discerned, and uncover the largest opportunities for improvement that warrant investment. Analytics is available at the tenant level.&#x20;

{% hint style="info" %}
To access Analytics, you need to have one of the following [Group roles](../../snyk-admin/user-roles/pre-defined-roles.md#group-level-permissions): Group Admin, Group Viewer, or a [Custom role](../../snyk-admin/user-roles/user-role-management.md#create-a-custom-role) with`report.read` permissions.
{% endhint %}

The Analytics view is structured as follows:

* [Issues Analytics](issues-analytics.md) - provides the exposure and performance details of Snyk issues in Groups and Organizations while focusing on the issue introduction method (baseline, preventable, or non-preventable).
* [Application Analytics](application-analytics.md) - provides data analytics for reviewing and comparing assets and issues metrics at the level of asset classes, applications, or code owners.

{% hint style="warning" %}
Application Analytics is available only to Snyk AppRisk Pro users. &#x20;
{% endhint %}

The following table presents an overview of the features available for both Issues Analytics and Application Analytics.

| Issues Analytics                                                                                                                                                                                                                           | Application Analytics                                                                                                                                                                                                                                                                                              |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <ul><li>Data filtered by default on critical and high-severity issues.</li><li>Drill down to see the way that issues were introduced.</li><li>Issues framework: categorized based on Exposure, Manage, Prevention, and Coverage.</li></ul> | <ul><li>Data filtered based on assets, applications, and code owners (teams).</li><li>Helps you to identify and take action on risk, coverage gaps, and association gaps.</li><li>Asset class view</li><li>Application and owner view</li><li>Surface coverage gap</li><li>Comparison and prioritization</li></ul> |

{% hint style="info" %}
The specific features and availability of both products may vary as they continue to evolve. For the latest information, refer to the respective product documentation.
{% endhint %}
