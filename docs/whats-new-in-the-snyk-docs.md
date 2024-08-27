---
cover: .gitbook/assets/Snyk General Banner.webp
coverY: 0
---

# What's new in the Snyk docs?

The most recent updates include significant changes to the user docs, such as features added or removed, structure changes that affect how you find relevant information, and other improvements aimed at enhancing your interaction with the Snyk knowledge base.

## July 2024

### Snyk AppRisk

* [Asset inventory filtering](manage-assets/assets-inventory-components.md#asset-tabs) describes the new, simplified view that provides an improved experience of filtering the assets.
* The [Asset inventory layouts](manage-assets/assets-inventory-layouts.md#inventory-layouts) have been renamed to better reflect their functionality.
* Four new SCM integrations are now available for Snyk AppRisk:&#x20;
  * [Atlassian Compass](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/application-context-for-scm-integrations.md#atlassian-compass)
  * [Harness](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/application-context-for-scm-integrations.md#harness)
  * [OpsLevel](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/application-context-for-scm-integrations.md#opslevel)
  * [Datadog Service Catalog](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/application-context-for-scm-integrations.md#datadog-service-catalog)
* The Snyk AppRisk documentation section has been reorganized to enhance visibility and simplify the adoption of Snyk AppRisk. Here is where you can find the main features:
  * Inventory - [Manage assets](manage-assets/) section
  * Issues - [Prioritize issues for fixing](manage-risk/prioritize-issues-for-fixing/#prioritization-based-on-risk) section
  * Policies - [Assets policies](manage-risk/policies/assets-policies/) section
  * Integrations - [Snyk SCM integrations](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#group-level-snyk-apprisk-scm-integrations) and [Integrate with Snyk](integrate-with-snyk/#integrations-for-snyk-apprisk) sections
  * Snyk AppRisk - [Scan with Snyk](scan-using-snyk/snyk-apprisk/) section
  * Analytics - [Manage risk](manage-risk/enterprise-analytics/application-analytics.md) section

### Snyk Integrations

* A comparison of the GitHub and GitHub Enterprise integrations functions now resides on the [SCM, IDE, and CI/CD integrations](scm-ide-and-ci-cd-integrations/#github-vs-github-enterprise) page.
* Steps for [migrating from the GitHub integration to the GitHub Enterprise integration](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/github.md#migrate-to-the-github-enterprise-integration) now reside on the GitHub integration page.
* The [Snyk SCM Integrations](https://docs.snyk.io/scm-ide-and-ci-cd-integrations/snyk-scm-integrations) page now contains information critical to using these integrations successfully in your SDLC. This includes:
  * Organizing integrations by [Group](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#group-level-snyk-apprisk-scm-integrations) and [Organization](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#organization-level-snyk-scm-integrations) level in line with Snyk AppRisk functionality
  * [Git repository cloning](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#snyk-git-repository-cloning) details
  * [Deployment recommendations](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#deployment-order-recommendations) for Enterprise customers
  * [User permissions and access scope requirements](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#user-permissions-and-access-scope-requirements) for each SCM integration
  * Instructions on how to generate [integrated SCM tokens for Snyk Broker](scm-ide-and-ci-cd-integrations/snyk-scm-integrations/#integrated-scm-tokens-for-snyk-broker)

### **Snyk API**

* The API documentation now provides the API Reference and explanatory documentation in the [API section](snyk-api/).
* The [API End of Life (EOL) process and migration guides](api-end-of-life-eol-process-and-migration-guides/) are now published and updated to support the process, which began in July.

### **Other updates**

* **Snyk Reports:** The [issue column dictionary](manage-risk/reporting/issue-columns-dictionary.md#issue-vulnerability-details) includes new filters and columns for Jira (JIRA ISSUES LIST, LATEST JIRA ISSUE) and EPSS (EPSS SCORE, EPSS PERCENTILE). This allows you to manage your work with Jira and to include EPSS in your prioritization steps.
* **Snyk Security:** Snyk has improved the prioritization workflow and risk assessment by adopting [CVSS V4.0](manage-risk/prioritize-issues-for-fixing/severity-levels.md#severity-levels-and-cvss) as the default evaluation for new vulnerabilities.
* **Fix code vulnerabilities automatically:** [DeepCode AI Fix](scan-with-snyk/snyk-code/manage-code-vulnerabilities/fix-code-vulnerabilities-automatically.md#deepcode-ai-fix-language-support) is now available in AWS Environments and JetBrains IDEs. If you use AWS multi-tenant environments, turn on the Snyk Preview [Snyk Code Fix Suggestions](scan-with-snyk/snyk-code/manage-code-vulnerabilities/fix-code-vulnerabilities-automatically.md#enable-deepcode-ai-fix) and retest with Snyk in your IDE.









