# Semantic Test Package

## About
Simple test repo to experiment with semantic-release, automatic versioning, and Github actions.

Publishes [jcowdy-semantic-test-pkg](https://www.npmjs.com/settings/jcowdy/packages) to npm.

## Setup
* Create a [Github personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) with repo level access.
* Create a [npm access token](https://docs.npmjs.com/creating-and-viewing-access-tokens): choose the "automation" type to skip 2FA in the publish action
  * This still requires 2FA to be enabled on your account!
* In project settings --> secrets --> actions: Add `GH_TOKEN` and `NPM_TOKEN`.

## Versioning
 Uses [conventional commit messages (Angular)](https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format) to determine if the next version should be a patch/minor/major.

## Publishing
* Automatically publishes to the npm registry using the [relase workflow](./github/workflows/release.yml).
* Only changes to the master branch are published.