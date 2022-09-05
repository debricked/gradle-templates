<img src="https://debricked.com/build/images/blueLogo.d39f7709.svg" alt="debricked" width="50%"  align="top"/>  

# Gradle templates
Here you find templates for integrating your Gradle repository with us.

In order for us to analyse all dependencies in your Gradle project, a file containing the resolved dependency tree has to be created prior to scanning.

This can be done by running Gradle `dependencies` command and storing the output in a file called `.debricked-gradle-dependencies.txt`.  
All examples in this repository generates that tree file.  
The command that is run prior to scanning is:
```sh
sh ./gradlew dependencies > .debricked-gradle-dependencies.txt
```
### Performance tip
Does your `.debricked-gradle-dependencies.txt` take a long time to create?  
Make sure to **cache** `.debricked-gradle-dependencies.txt` or the [Gradle Build Cache](https://docs.gradle.org/current/userguide/build_cache.html) between runs where your build is the same!

Different CI/CD tools offer different support for this. Below you can find docs on how set this up:
- GitHub Actions: [docs](https://github.com/actions/cache)
- CircleCI: [docs](https://circleci.com/docs/2.0/caching/)
- BuildKite: [docs](https://github.com/buildkite/gradle-docker-example) (In BuildKite docker volumes comes in handy)
- GitLab CI/CD: [docs](https://docs.gitlab.com/ee/ci/caching/)
- Azure Pipelines: [docs](https://docs.microsoft.com/en-us/azure/devops/pipelines/release/caching?view=azure-devops#gradle)

## GitHub Actions [![Debricked scan](https://github.com/debricked/gradle-templates/actions/workflows/debricked.yml/badge.svg)](https://github.com/debricked/gradle-templates/actions/workflows/debricked.yml)
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/github.html#github-actions)
- [See template](.github/workflows/debricked.yml)

## CircleCI [![CircleCI](https://circleci.com/gh/debricked/gradle-templates/tree/main.svg?style=svg)](https://circleci.com/gh/debricked/gradle-templates/tree/main)
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/circle-ci.html)
- [See template](.circleci/config.yml)

## BuildKite [![Build status](https://badge.buildkite.com/cfa55dd090d068f438bc72c2a1a79b2052da8d9c77dcd7edbf.svg)](https://buildkite.com/debricked/gradle-templates)
- Add Debricked token variable. [Read more](https://buildkite.com/docs/pipelines/environment-variables#defining-your-own)
- [See template](.buildkite/pipeline.yml)

## GitLab CI/CD
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/gitlab.html#integrating-using-an-access-token)
- [See template](.gitlab-ci.yml)

## Azure Pipelines
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/azure-devops.html)
- [See template](azure-pipelines.yml)

## Argo Workflows
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/argo-workflows.html)
- [See template](argo.yml)

## Travis CI
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/travis.html)
- [See template](.travis.yml)

## Bitbucket
- Add Debricked token variable. [Read more](https://debricked.com/docs/integrations/ci-build-systems/bitbucket.html)
- [See template](bitbucket-pipelines.yml)