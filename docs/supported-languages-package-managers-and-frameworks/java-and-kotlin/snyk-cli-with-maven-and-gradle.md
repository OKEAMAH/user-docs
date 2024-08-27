# Snyk CLI with Maven and Gradle

The Snyk CLI tests Maven and Gradle Projects as follows:

* **Snyk CLI with Gradle**: To build the dependency graph, Snyk integrates with Gradle and inspects the dependencies returned by the build. The following manifest files are supported: `build.gradle` (Groovy DSL) and `build.gradle.kts` (Kotlin DSL).
* **Snyk CLI with Maven**: To build the dependency tree, Snyk integrates with Gradle and inspects the dependencies returned by the build. The following manifest files are supported: `pom.xml`.

The following lists steps to start scanning your dependencies. It covers basic commands, such as `snyk test` and `snyk monitor`. To check the full list, see [CLI commands and options summary](../../snyk-cli/cli-commands-and-options-summary.md).&#x20;



| Package manager     | Test help                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 | Monitor help                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Maven               | <p><code>--maven-aggregate-project</code><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="https://docs.snyk.io/snyk-cli/commands/test#options-for-maven-projects">Options for Maven Projects</a> page for more details.<br><br>Example for aggregate projects:<br><code>snyk test --maven-aggregate-project</code><br><br>Example for non-aggregate projects: <code>snyk test --all-projects</code><br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> Be sure to execute the options in the same directory as the root pom.xml file. </p>                                                                                                                                                                                                                                                                                                                                                                                                        | <p><code>--maven-aggregate-project</code><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="https://docs.snyk.io/snyk-cli/commands/monitor#options-for-maven-projects">Options for Maven Projects</a> page for more details.<br><br>Example for aggregate projects:<br><code>snyk monitor --maven-aggregate-project</code><br><br>Example for non-aggregate projects: <code>snyk monitor --all-projects</code><br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> Be sure to execute the options in the same directory as the root pom.xml file. </p>                                                                                                                                                                                                                                                                                                                                                                                     |
| Gradle              | <p><code>--sub-project=&#x3C;NAME></code>, <code>--gradle-sub-project=&#x3C;NAME></code> - Test a specific Gradle sub-project.</p><p></p><p><code>--all-sub-projects</code> - Test all Gradle sub-projects.</p><p></p><p><code>--all-projects</code> - Test all Gradle projects.</p><p></p><p><code>--configuration-matching=&#x3C;CONFIGURATION_REGEX></code> - Resolve dependencies using the first configuration that matches the specified Java regular expression.</p><p></p><p>-<code>-configuration-attributes=&#x3C;ATTRIBUTE>[,&#x3C;ATTRIBUTE>]...</code>- Select certain values of configuration attributes to install and resolve dependencies.</p><p></p><p><code>--init-script=&#x3C;FILE></code> - Used for projects with a Gradle initialization script.</p><p></p><p><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="https://docs.snyk.io/snyk-cli/commands/test#options-for-gradle-projects">Options for Gradle Projects </a>page for more details.</p><p></p> | <p><code>--sub-project=&#x3C;NAME></code>, <code>--gradle-sub-project=&#x3C;NAME></code> - Monitor a specific Gradle sub-project.</p><p></p><p><code>--all-sub-projects</code> - Monitor all Gradle sub-projects.</p><p></p><p><code>--all-projects</code> - Monitor all Gradle projects.</p><p></p><p><code>--configuration-matching=&#x3C;CONFIGURATION_REGEX></code> - Resolve dependencies using the first configuration that matches the specified Java regular expression.</p><p></p><p><code>--configuration-attributes=[,]...</code> - Select certain values of configuration attributes to install dependencies and perform dependency resolution.</p><p></p><p><code>--init-script=&#x3C;FILE></code> - Used for projects with a Gradle initialization script.<br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="https://docs.snyk.io/snyk-cli/commands/monitor#options-for-gradle-projects">Options for Gradle Projects</a> page for more details.</p> |
| Build tools         | <p><code>snyk test -- [&#x3C;context-specific_options>]</code><br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="https://docs.snyk.io/snyk-cli/commands/test#options-for-build-tools">Options for build tools</a> page for more details.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | <p><code>snyk monitor -- [&#x3C;context-specific_options>]</code><br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="https://docs.snyk.io/snyk-cli/commands/monitor#options-for-build-tools">Options for build tools</a> page for more details.</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Unmanaged JAR files | <p><code>--scan-unmanaged</code> - Test unmanager files <br></p><p><code>--scan-unmanaged --file=&#x3C;JAR_FILE_NAME></code> - Test individual JAR, WAR, and AAR files<br></p><p><code>--scan-all-unmanaged</code> - Auto-detect Maven, JAR, WAR, and AAR files recursively from the current folder.<br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="../../snyk-cli/commands/test.md#scan-all-unmanaged">Options for unmanaged JAR files</a> page for more details. </p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  | <p><code>--sub-project=&#x3C;NAME></code>, <code>--gradle-sub-project=&#x3C;NAME></code> - Monitor a specific Gradle sub-project.</p><p></p><p><code>--all-sub-projects</code> - Monitor all Gradle sub-projects.</p><p></p><p><code>--all-projects</code> - Monitor all Gradle projects.</p><p></p><p><code>--configuration-matching=&#x3C;CONFIGURATION_REGEX></code> - Resolve dependencies using only configuration(s) that match the specified Java regular expression.</p><p></p><p><code>--init-script=&#x3C;FILE></code> - Used for projects with a Gradle initialization script.<br><br><span data-gb-custom-inline data-tag="emoji" data-code="2139">ℹ️</span> See the <a href="../../snyk-cli/commands/monitor.md#scan-all-unmanaged">Options for unmanaged JAR files</a> page for more details.</p>                                                                                                                                                                                                 |

## CLI help for Maven Projects

A **Maven aggregate Project** is one that uses modules and inheritance.

When scanning these types of Projects, Snyk performs a compile to ensure all modules are fixable by the Maven reactor.

*   To **scan aggregate Projects**, use the `--maven-aggregate-project` option:

    ```
    snyk test --maven-aggregate-project
    ```
*   To **scan non-aggregate Projects**, use the `--all-projects` option:

    ```
    snyk test --all-projects
    ```

The same options can be used with `snyk monitor`.

Be sure to execute the options in the same directory as the root pom.xml file.

Each of the individual sub-projects appears as a separate Snyk Project in the Web UI.

### **Examples of how to use Maven-specific options with the Snyk CLI**

Test a specific Maven profile called “prod”.

```
snyk test -- -prod
```

Add a system property from your pom.xml file.

Example:

The package version appears in your pom.xml

```
${pkg_version}
```

Define the system property like this:

```
snyk test -- -Dpkg_version=1.4
```

## CLI help for Gradle Projects

Gradle build can consist of several sub-projects, where each sub-project has its own build.gradle, while the root Project is the only one that also includes a `settings.gradle` file. Sub-projects depend on the root ProjectProjects but can be configured otherwise.

By default, Snyk CLI scans only the current Project, the Project in the root of the current folder, or the Project that is specified by `--file=path/to/build.gradle`).

*   To scan all Projects at once (recommended), use the `--all-sub-projects` option:

    ```
    snyk test --all-sub-projects
    ```

Each of the individual sub-projects appears as a separate Snyk Project in the Web UI.

*   To scan a specific Project (for example, myapp):

    ```
    snyk test --sub-project=myapp
    ```

### Gradle configurations

Gradle dependencies are declared for a particular scope; each scope is represented by Gradle with the help of [Configurations](https://docs.gradle.org/current/userguide/declaring\_dependencies.html#sec:what-are-dependency-configurations). For example:

* **implementation**: configuration for dependencies required at compile time and runtime, but not exposed to consumers.&#x20;
* **api**: configuration for dependencies required at compile time and runtime, and exposed to consumers.&#x20;
* **compileOnly**: configuration for dependencies required only at compile time.&#x20;
* **runtimeOnly**: configuration for dependencies required only at runtime.&#x20;
* **compileClasspath**: configuration for dependencies required at compile time.

In most cases, Snyk will include all the dependencies in the **compileClasspath** configuration, but this can vary in some circumstances.

To test a specific configuration:

* Use the `--configuration-matching` option with a [Java regular expression](https://docs.oracle.com/javase/tutorial/essential/regex/) (case-insensitive) as its parameter. Note that only the first configuration that matches is tested.
* If the different sub-projects include different configurations, scan each sub-project separately.

Examples of how you can use the --configuration-matching option

* `--configuration-matching=compile` will match compile, testCompile, compileOnly, and so on.
* `--configuration-matching=^compile$` will match only compile.
* `--configuration-matching='^(debug|release)compile$'` will match debugCompile and releaseCompile.
* `--configuration-matching='^(?!.*test).*$'` will match all configurations _except_ those containing the string "test".

### Android build variants

Android Gradle supports creating different versions of your app by configuring [build variants.](https://developer.android.com/studio/build/build-variants)

Because the Snyk default behavior is to merge all available configurations, the iterated variants cause a clash of configurations that can't be merged.

In these situations, the Snyk scan fails with an error from Gradle which may contain one of the following messages:

* Cannot choose between the following configurations of `project :mymodulewithvariants`
* Cannot choose between the following variants of `project :mymodulewithvariants`
* Could not select value from candidates

To avoid such conflicts:

*   **Use a specific configuration(s):** if you know of a build configuration that has all the required attributes and the configuration is identical across all sub-projects included in the test, specify that configuration.\
    For example:

    ```
    --configuration-matching=prodReleaseRuntimeClasspath
    ```
*   **Explicitly specify the dependency configuration:** modify intra-project dependencies in your build.gradle file(s) to use a specific configuration

    ```
      dependencies {
          implementation project(path: ':mymodulewithvariants', configuration: 'default')
      }
    ```
*   **Suggest configuration attributes:** if you receive an error when running the command, the error may indicate which attribute values are available, while the error details from Gradle also indicate which dependency variants match which attributes. Using these details, add the attribute filter option.\
    For example:

    ```
    snyk test --configuration-attributes=buildtype:release,usage:java-runtime,mode:demo
    ```

    matches the variants using `com.android.build.api.attributes.BuildTypeAttr=release` and `org.gradle.usage=java-runtime`

### Daemon

By default, Snyk passes `gradle build --no-daemon` in the background when running `snyk test` and `snyk monitor` on Windows.&#x20;

If you see `snyk test` or `snyk monitor` fail on other operating systems because of daemon-related issues, try adding the `--no-daemon` flag to the Snyk command or set `GRADLE_OPTS: '-Dorg.gradle.daemon=false'`.&#x20;

See the [Gradle documentation](https://docs.gradle.org/current/userguide/gradle\_daemon.html#sec:disabling\_the\_daemon) for tips on disabling the daemon.

### Lockfiles

If your Gradle Project makes use of a single `gradle.lockfile` or multiple `*.lockfile` per configuration, you may see the following issue:

{% code overflow="wrap" %}
```
Gradle Error (short): > Could not resolve all dependencies for configuration ':compileOnly'. > Locking strict mode: Configuration ':compileOnly' is locked but does not have lock state.
```
{% endcode %}

The **compileOnly configuration** **has been deprecated,** and even if your Project successfully generates a lockfile, the `compileOnly` state is not included because this configuration cannot be resolved.&#x20;

Only resolvable configurations compute a dependency graph. To solve this issue, Snyk suggests you update your `build.gradle` containing `dependencyLocking` logic with the following instruction**:**

```
compileOnly {resolutionStrategy.deactivateDependencyLocking() }
```

This ignores the compileOnly and saves only the necessary information to analyze your Project.

### Getting help

If you are having any trouble testing your Gradle Projects with Snyk, collect the following details and send them to Snyk at [support@snyk.io](mailto:support@snyk.io):

* `build.gradle`
* `settings.gradle` (especially if Snyk did not pick up a version of a package)
* The output from the following commands:
  * `$ snyk test -d`
  * `$ gradle dependencies -q`
