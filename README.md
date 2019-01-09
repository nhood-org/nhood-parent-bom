[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![CircleCI](https://circleci.com/gh/nhood-org/nhood-parent-bom.svg?style=shield)](https://circleci.com/gh/nhood-org/nhood-parent-bom)

# Parent BOM

Project is part of [nhood](https://github.com/nhood-org/nhood-docs) project. 

The `nhood-parent-bom` is a maven parent project for all `nhood` maven projects.

## Pre-requisites

- Java 11
- Maven

## Build

In order to build the project use the following maven command:

```bash
mvn clean install
```

## Test

In order to test the project use the following maven command:

```bash
mvn clean test
```

## Run

Project is not a stand-alone application therefore it cannot be run.

## CI/CD

Project is continuously integrated with `circleCi` pipeline that link to which may be found [here](https://circleci.com/gh/nhood-org/workflows/nhood-parent-bom)

Pipeline is fairly simple:

1. Build and test project
2. Deploy new snapshot version to [nhood maven repository](https://github.com/nhood-org/nhood-repository/tree/mvn-repo/com/h8/nh)

Configuration of CI is implemented in `.circleci` and `.circleci.setting.xmls`.

## Versioning

In order to release version, send the following API request to circleCI:

```bash
curl -u <CIRCLE_CI_USER_TOKEN> -d build_parameters[CIRCLE_JOB]=release https://circleci.com/api/v1.1/project/github/nhood-org/nhood-parent-bom/tree/master
```

## License

`nhood-parent-bom` is released under the MIT license:
- https://opensource.org/licenses/MIT
