# Access requirements

When you are using Snyk applications like the [CLI ](../getting-started-with-the-snyk-cli.md)or [IDE integrations](../../scm-ide-and-ci-cd-integrations/snyk-ide-plugins-and-extensions/), certain local and remote resources must be accessible. This documentation explains how to harden your system without affecting Snyk functionality.

## Local filesystem

The required filesystem access may vary by product.

* CACHE\_PATH (Read,Write,Execute)
  * Windows: `C:\\Users\\<USERNAME>\\AppData\\Local\\snyk`
  * Linux/Alpine: `/home/<USERNAME>/.cache/snyk`
  * macOS: `/Users/<USERNAME>/Library/Caches/snyk`
* CONFIG\_PATH (Read,Write)
  * Windows: `%USERPROFILE%\\.config\\configstore`
  * Linux: `$HOME/.config/configstore`
  * macOs: `$HOME/.config/configstore`

## Network resources

### Required

* api.\<SNYK\_INSTANCE>.io:443
* app.\<SNYK\_INSTANCE>.io:443

### Optional

* deeproxy.snyk.io:442 (for snyk code)
* downloads.snyk.io:443 (depending on features  used)
* static.snyk.io:443 (depending on features used )
* snyk.io:443 (depending on features used)
* \*_.sentry.io:443 (error reporting)_
* \*_.amplitude.com:443 (analytics)_
