# How to obtain and use your Snyk API token

{% hint style="info" %}
Before authenticating, ensure your endpoints are set correctly. For a list of URLs, see [Regional hosting and data residency](../working-with-snyk/regional-hosting-and-data-residency.md).
{% endhint %}

## Obtain your personal Snyk API token

Follow these steps to obtain your personal Organization Snyk API token:

1. Find your token in your [General Account Settings](https://app.snyk.io/account) after you register with Snyk and log in.
2. In the **key** field, **Click to show**.
3. Highlight and copy the API key.

If you want a new API token, select **Revoke & Regenerate.** This will make the previous API token invalid.

## How to use personal and service account tokens&#x20;

Your Snyk API token is a personal token available under your user profile. The Snyk API token is associated with your Snyk Account and not with a specific Organization.

Free, Team, and Trial plan users have access only to this personal token under the user profile. The **personal token can be used** to authenticate with:

* The Snyk CLI running on a local or a build machine
* An IDE, when setting a token manually
* A CI/CD integration

Enterprise users have access to a personal token under their profile and to service account tokens. For details, see [Service accounts](../enterprise-setup/service-accounts/).

* **Enterprise users should use a service account** to authenticate for any kind of automation. This includes, but is not limited to, CI/CD scanning with the CLI or build system plugins and automations, including the API.
* **Enterprise users should use the personal token** under their user profile for:
  * Running the CLI locally on their machine
  * Authenticating with the IDE manually
  * Running API calls one time, for example, to test something

For more information on the personal Snyk API token, see the following pages: [Authenticate to use the CLI](../snyk-cli/authenticate-to-use-the-cli.md) and [Authentication for API](../snyk-api/rest-api/authentication-for-api/).
