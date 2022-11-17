# github-action-nitro-android

<!-- action-docs-description -->
### Description

A Gihub Action for building React Native apps with Nitro
<!-- action-docs-description -->

### Environment Variables

| name          | description                                                                                                                             |
| ------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| NITRO_LICENSE | A secured string containing the license required to run optimized builds. If not provided, invalid or expired it will run in slow mode. |

<!-- action-docs-inputs -->
### Inputs

| parameter | description | required | default |
| --- | --- | --- | --- |
| root-directory | The directory within your project, in which your code is located. Leave this field empty if your code is not located in a subdirectory" | `false` | . |
| flavor | The product flavor for Gradle build variant | `false` |  |
| version-name | The version name for the app | `false` |  |
| version-code | The version code for the app | `false` |  |
| disable-version-name-from-package-json | Disable automatic version name configuration. By default will get the 'version' field from package.json and set the version name. Available Options: (`yes` / `no`) | `false` |  |
| disable-version-code-auto-generation | Disable automatic version code generation. By default will generate a timestamp based number and set the version code. Available Options: (`yes` / `no`) | `false` |  |
| keystore-url | Keystore url | `false` |  |
| keystore-password | Keystore password | `false` |  |
| keystore-key-alias | Keystore alias | `false` |  |
| keystore-key-password | Keystore key password | `false` |  |
| cache-provider | Cache provider where cache artifacts will be persisted. Available Options: (`fs`: File system / `github`: Uses Github cache action / `s3`: Amazon - Simple Storage Service) | `false` | s3 |
| disable-cache | When setting this option to `yes` build cache optimizations won't be performed.  Available Options: (`yes` / `no`) | `false` |  |
| cache-env-var-lookup-keys | List of env var keys for lookup to determine cache fingerprint. A list of `\|` separated values with env variable keys to lookup to determine whether the build should be cached or not | `false` |  |
| cache-file-lookup-paths | List of files for lookup to determine cache fingerprint. A list of `\|` separated value paths (relative to the root of the repo or absolute) to lookup in order to determine whether the build should be cached or not | `false` |  |
| disable-metro-cache | Setting this field to yes will disable the React Native Metro cache feature | `false` |  |
| pre-install-command | Run command prior to install project dependencies (e.g. `rm -rf ./some-folder`) | `false` |  |
| pre-build-command | Run command prior to start building the app (e.g. `yarn tsc && yarn test`) | `false` |  |
| post-build-command | Run command once build successfully finished (e.g. `yarn publish`) | `false` |  |
| output-directory | The path to the directory where to place all of Nitro's output files | `false` |  |
| entry-file | The entry file for bundle generation | `false` |  |
| debug | Enable verbose logs. Available Options: (`yes` / `no`) | `false` |  |
| fail-safe | Runing the app in this mode allows you to prevent the build to fail but you can check the status in further steps | `false` |  |
<!-- action-docs-inputs -->

<!-- action-docs-outputs -->
### Outputs

| parameter | description |
| --- | --- |
| nitro-build-status | The status of the latest build (success / failure) |
| nitro-output-dir | The path to the directory where to place all of Nitro's output files |
| nitro-logs-path | The full path to access the build log |
| nitro-deploy-path | The full path to access the build artifacts |
| nitro-summary-path | The full path to access the build summary report |
<!-- action-docs-outputs -->

<!-- action-docs-runs -->
### Runs

This action is a `composite` action.
<!-- action-docs-runs -->
