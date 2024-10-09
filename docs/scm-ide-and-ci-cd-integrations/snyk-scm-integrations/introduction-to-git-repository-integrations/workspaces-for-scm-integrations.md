# Workspaces for SCM integrations

{% hint style="warning" %}
Workspaces **significantly** improves the accuracy and reliability of Snyk’s SCM integration results, especially for large-scale enterprise environments. This capability also supports additional functionality and improvements we have planned in the future. For these reasons, Snyk **strongly recommends** [enabling this option](workspaces-for-scm-integrations.md#manage-workspaces) by default at your Group level.
{% endhint %}

## The importance of Workspaces: Improved reliability and accuracy

Snyk believes Workspaces is a significant step forward in providing you with the most **reliable** and **accurate** vulnerability detection possible.

### How Workspaces supports more reliable results

Traditionally, Snyk has accessed repository contents using SCM APIs, which impose primary and secondary rate limits, and content limits. For example, the GitHub.com APIs are rate-limited to allow only a certain number of requests per hour, and there is a limit on the number of tree entries that can be retrieved from the Git database.

When repository contents are retrieved over these APIs, these limitations inhibit Snyk’s providing a complete analysis in a number of ways, especially across a very large number of repositories, or for repositories containing more than 100,000 files, sometimes referred to as monorepos.

Through Workspaces, these limitations are removed.

### How Workspaces supports more accurate results

The accuracy of results is improved in a number of ways through cloning. Since Snyk can access a complete view of a source code repository at a specific commit SHA, including repositories containing more than 100,000 files, the analysis is also more complete through cloning.

## Snyk data ingestion

When Workspaces is enabled, Snyk will ingest, through configured SCM integrations, a temporary and shallow clone of repository contents at a given commit and all commit metadata (including the commit message, authors, and timestamp).

{% hint style="info" %}
For more information on Snyk data processing and safeguards concerning Git repo cloning, see [Cache retention period related to vulnerability source data](../../../working-with-snyk/how-snyk-handles-your-data.md#cache-retention-period-related-to-vulnerability-source-data) and [Safeguards Snyk puts in place to ensure data is secure](../../../working-with-snyk/how-snyk-handles-your-data.md#safeguards-snyk-puts-in-place-to-ensure-data-is-secure).
{% endhint %}

## Git protocols used by Workspaces&#x20;

Repositories are cloned using HTTPS. SSH-based clones are currently unavailable.

## Snyk Broker interactions

Brokered connections are supported when Git operations are allowed through Broker.

{% hint style="warning" %}
This will override restrictions from `accept.json`. For more information, see [Clone capability with Broker for Docker](../../../enterprise-setup/snyk-broker/install-and-configure-snyk-broker/advanced-configuration-for-snyk-broker-docker-installation/snyk-code-clone-capability-with-broker-for-docker.md).
{% endhint %}

## Manage Workspaces

The Workspaces feature is managed through the **Integrations settings** page on the Group or Organization level. To do so, you must be a Snyk Group Admin or Snyk Organization Admin.

When enabled at the Group level, all Organizations within that Group will have Workspaces enabled.

The Workspaces feature can be enabled for individual organizations within a Group, even if disabled at the Group level.

While you can choose to disable the Workspaces feature, it is important to understand doing so will hinder Snyk’s ability to scan repositories in two specific ways:

1. **Frequency of scanning**: With Workspaces disabled, Snyk will analyze repository content through SCM APIs, which typically impose primary and secondary rate limits, and content limits. For example, the GitHub.com APIs are rate-limited to allow only a certain number of requests per hour, which hinders Snyk’s ability to analyze a large number of repositories in any one hour.
2. **Completeness of scanning**: With the Workspaces feature disabled, Snyk will analyze repo content through SCM APIs, which typically limit the number of tree entries that can be retrieved from the Git database, potentially leading to missed vulnerabilities. This impacts analysis of repositories containing a large number of files, sometimes referred to as monorepos.
