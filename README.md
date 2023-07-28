<div align="left">
  <img src="https://github.com/open-horizon/.github/blob/master/profile/open-horizon-color.png" alt="Badge" width="auto" height="50">
  
<h1 align="center">Open Horizon Releases</h1>

<p align="center">
  <a href="https://github.com/blakep7/Open-Horizon-Release/releases/latest">
    <img src="https://img.shields.io/github/v/release/blakep7/Open-Horizon-Release" alt="Release">
    <img src="https://img.shields.io/github/release-date/blakep7/Open-Horizon-Release" alt="Release Date">
  </a>
</p>

<p align="center">
  This repository is dedicated to releasing Open Horizon components and tracking their versions across repositories.
</p>

## Table of Contents

- [Introduction](#introduction)
- [Release Manager Workflow](#release-manager-workflow)
- [Contributing](#contributing)
- [License](#license)

## Introduction

Open Horizon Releases is a central repository aimed at managing and coordinating the release process for various Open Horizon components. Open Horizon is an open-source, edge-computing platform for managing the service software lifecycle of containerized workloads and related machine learning assets. It enables autonomous management of applications deployed to distributed webscale fleets of edge computing nodes and devices without requiring on-premise administrators.

This repository serves as the single source of truth for version tracking and the release process. It consolidates version information from multiple repositories and provides guidelines for creating releases and distributing components.

## Release Manager Workflow

The Release Manager Workflow is used to tagging and releasing of Open Horizon components. It ensures consistency and reliability in the release process. Here's a step-by-step guide on how to use the Release Manager Workflow in this repository:

### 1. Creating a New Release

When it's time to create a new release for any Open Horizon component, follow these steps:

- **Step 1:** Generate your Release Versions JSON, it must include all of the fields within the example below.

```json
{   
    "amd64_agbot": "2.31.0-1498",
    "amd64_anax": "2.31.0-1498",
    "amd64_anax_k8s": "2.31.0-1498",
    "amd64_cloud-sync-service": "1.10.1-1498",
    "amd64_edge-sync-service": "1.10.1-1498",
    "amd64_exchange-api": "2.117.0-1163",
    "amd64_vault": "1.1.2-806",
    "fdo-owner-services": "2.31.0-1498",
    "sdo-owner-services": "1.11.16-1083"
}
```

- **Step 2:** Clone the forked repository to your local machine.

- **Step 3:** Update the version information of the component in the appropriate JSON file under the [releases](releases) directory. Make sure to follow semantic versioning (MAJOR.MINOR.PATCH).

- **Step 4:** Commit the changes with a descriptive message about the version update.

- **Step 5:** Create a pull request (PR) to the main repository.

- **Step 6:** The Release Manager will review the changes and merge the PR if everything looks good.

### 2. Release and Tagging

Once the pull request is merged, the Release Manager will follow these steps to release and tag the component:

- **Step 1:** The Release Manager will create a new GitHub release using the version information provided in the PR.

- **Step 2:** The Release Manager will tag the component's repository with the corresponding version number.

- **Step 3:** The tagged release will trigger the CI/CD process for the component, and it will be available for use.

## Contributing

Contributions to Open Horizon Releases are welcome! If you have suggestions, bug reports, or want to contribute to the release process, please follow the guidelines in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

This project is licensed under the Apache License 2.0. See [LICENSE](LICENSE) for more details.

