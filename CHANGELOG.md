# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.0.1] - 2020-12-07
### Added
 - Initial release.
 - Common CI/CD tasks for basic Docker and Helm workflows.

## [0.0.2] - 2020-12-07
### Added
 - Enforce git tag filtering on all CircleCI jobs.

## [0.0.3] - 2020-12-07
### Changed
 - Split testing from publishing workflow.

## [0.1.1] - 2020-12-07
### Changed
 - Fix missing token on Helm build job.

## [0.1.2] - 2020-12-08
### Added
 - Common CI/CD tasks for basic Python workflows.

## [0.1.3] - 2020-12-10
### Added
 - Common CI/CD tasks for basic Terraform workflows.

## [0.1.4] - 2020-12-10
### Added
 - Standard example workflow with Python jobs.
### Changed
 - Pass build arguments into the Docker build job.

## [0.1.5] - 2020-12-17
### Changed
 - Bump `noos-ci` CLI version to v0.0.4.

## [0.1.6] - 2020-12-24
### Changed
 - Bump Helm CLI to v3.4.2.
 - Bump Helm CircleCI Orb to v1.1.2

## [0.1.7] - 2021-01-05
### Changed
 - Switch from `noos-ci` to `noos-inv` CI/CD SDK.
 - Bump `noos-tf` CLI version to v0.0.5.
 - Bump `noos-inv` CLI version to v0.0.5.
### Added
 - Pass install arguments for the Python venv installation.

## [0.1.8] - 2021-01-05
### Changed
 - Bump `pipenv` CLI version to v2020.11.15.
 - Bump `poetry` CLI version to v1.1.4.

## [0.1.9] - 2021-01-06
### Changed
 - Bump Python version to v3.8.6.

## [0.1.10] - 2021-01-08
### Changed
 - Downgrade `pipenv` CLI version to v2020.11.4.

## [0.1.11] - 2021-01-21
### Changed
 - Bump `noos-tf` CLI version to v0.0.6 (py38).
 - Bump `noos-inv` CLI version to v0.0.6 (py38).

## [0.1.12] - 2021-05-21
### Changed
 - Bump `noos-inv` CLI version to v0.0.7.
 - Pass optional `--file` argument to command docker.build.

## [0.1.13] - 2021-10-07
### Changed
 - Bump `noos-inv` CLI version to v0.0.8.

## [0.1.14] - 2021-11-29
### Changed
 - Switch orb executor to custom CircleCI Docker image (repo `noosenergy/circleci`).
### Added
 - Trigger Slack notifications on failed PyPi/Docker/Helm builds.

## [0.1.15] - 2022-09-01
### Changed
 - Bump Docker CLI to v20.10.14.
 - Bump Helm CLI to v3.9.0.
### Added
 - Publish Helm chart to either Chart Museum or AWS ECR registries.

## [0.1.16] - 2023-08-10
### Changed
 - Bump AWS CircleCI Orb to v4.0.0.
 - Bump Slack CircleCI Orb to v4.12.5.
 - Bump Helm CLI to v3.12.2.
 - Upgrade orb-tools dependency.
### Added
 - Put executor tag as a parameter.
 - Add orb-tools/review job.

## [0.1.17] - 2023-08-24
### Added
 - Add tag_only parameter to allow pushing image to the registry with one tag only, and without the tag "latest"
 - Add new CI job to the workflow: integration_test_docker_build_image_tag_only

## [0.2.0] - 2023-11-20
### Added
 - Add Docker buildx command for cross platform.

## [0.2.1] - 2023-11-21
### Added
 - Simplify the buildx command using a DRY config.

## [0.2.2] - 2023-11-28
### Added
 - Allow caching Docker intermediate layers.

## [0.2.3] - 2024-02-16
### Added
 - Add executor with postgres side-car container.

## [0.2.4] - 2024-05-08
### Added
 - Add circleci no_output_timeout parameter for docker build image.

## [0.3.0] - 2024-08-21
### Added
 - Add `uv` python package manager.`

## [0.3.1] - 2024-08-23
### Changed
 - Remove `uv` CI caching strategy (ensure pre-built wheels are cached).
 - Ensure CircleCI Python caching keys are coherent between root / branch and lock hash.
 - Add Python executor with a Timesacle side-car container.

## [0.3.2] - 2024-10-07
### Changed
 - Upgrade native Circle Orbs for AWS, Helm and Slack.
 - Upgrade Helm CLI to v3.16.1.

## [0.4.0] - 2024-10-09
### Added
 - Add AI PR Agent.
 - Add github command to post a comment in a PR.

## [0.4.1] - 2025-01-10
### Changed
 - Bump AWS CircleCI Orb to v5.1.2.
 - Bump Slack CircleCI Orb to v5.1.1.
 - Bump Helm CircleCI Orb to v3.1.0.
 - Bump orb-tools to v12.3.0.
