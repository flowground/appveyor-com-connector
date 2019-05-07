# ![LOGO](logo.png) AppVeyor MSP Connector

## Description

A generated MSP connector for the AppVeyor API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/appveyor.com/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T11:17:13+03:00

## API Description

AppVeyor is a hosted continuous integration service which runs on Microsoft
Windows.  The AppVeyor REST API provides a RESTful way to interact with the
AppVeyor service.  This includes managing projects, builds, deployments,
and the teams that build them.

Additional help and discussion of the AppVeyor REST API is available at
http://help.appveyor.com/discussions

This Swagger definition is an **unofficial** description of the AppVeyor
REST API maintained at https://github.com/kevinoid/appveyor-swagger
Please report any issues or suggestions for this Swagger definition at
https://github.com/kevinoid/appveyor-swagger/issues/new

#### API Conventions

Fields which are missing from update operations (`PUT` requests) are
typically reset to their default values.  So although most fields are not
technically required, they should usually be specified in practice.


## Authorization

Supported authorization schemes:
- API Key
## Actions

### Encrypt a value for use in StoredValue.

*Tags:* `Project`

### Get build artifacts

*Tags:* `Build`

#### Input Parameters
* `jobId` - _required_ - Build ID (`jobId` property of `BuildJob`)

### Download build artifact

*Tags:* `Build`

#### Input Parameters
* `jobId` - _required_ - Build ID (`jobId` property of `BuildJob`)
* `artifactFileName` - _required_ - File name (or path) of a build artifact file.
Corresponds to the `fileName` property of `ArtifactModel`.
URL-encoding of slashes in parameter values is optional.

### Download build log

*Tags:* `Build`

#### Input Parameters
* `jobId` - _required_ - Build ID (`jobId` property of `BuildJob`)

### Start build of branch most recent commit

*Tags:* `Build`

### Re-run build

> If `reRunIncomplete` is `true` and all jobs in the referenced build completed successfully, a 500 Internal Server Error is returned with the message "No failed or cancelled jobs in build with ID {buildId}".

*Tags:* `Build`

### Cancel build

*Tags:* `Build`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug
* `buildVersion` - _required_ - Build Version (`version` property of `Build`)

### Get collaborators

*Tags:* `Collaborator`

### Add collaborator

*Tags:* `Collaborator`

### Update collaborator

*Tags:* `Collaborator`

### Delete collaborator

*Tags:* `Collaborator`

#### Input Parameters
* `userId` - _required_ - User ID

### Get collaborator

*Tags:* `Collaborator`

#### Input Parameters
* `userId` - _required_ - User ID

### Start deployment

*Tags:* `Deployment`

### Cancel deployment

*Tags:* `Deployment`

### Get deployment

*Tags:* `Deployment`

#### Input Parameters
* `deploymentId` - _required_ - Deployment ID (`deploymentId` property of `Deployment`)

### Get environments

*Tags:* `Environment`

### Add environment

*Tags:* `Environment`

### Update environment

*Tags:* `Environment`

### Delete environment

*Tags:* `Environment`

#### Input Parameters
* `deploymentEnvironmentId` - _required_ - Deployment Environment ID (`deploymentEnvironmentId` property of `DeploymentEnvironment`)


### Get environment deployments

*Tags:* `Environment`

#### Input Parameters
* `deploymentEnvironmentId` - _required_ - Deployment Environment ID (`deploymentEnvironmentId` property of `DeploymentEnvironment`)


### Get environment settings

*Tags:* `Environment`

#### Input Parameters
* `deploymentEnvironmentId` - _required_ - Deployment Environment ID (`deploymentEnvironmentId` property of `DeploymentEnvironment`)


### Get projects

*Tags:* `Project`

### Add project

*Tags:* `Project`

### Update project

*Tags:* `Project`

### Get status badge image for a project with a public repository

*Tags:* `Project`

#### Input Parameters
* `branch` - _optional_ - Repository Branch
* `svg` - _optional_ - Return an SVG image instead of PNG?  Exclusive with `retina`.
* `retina` - _optional_ - Return a larger image suitable for retina displays?  Exclusive with `svg`.
* `passingText` - _optional_ - Text to show in badge when build is passing.
* `failingText` - _optional_ - Text to show in badge when build is failing.
* `pendingText` - _optional_ - Text to show in badge when build is pending.

### Get project status badge image

*Tags:* `Project`

#### Input Parameters
* `svg` - _optional_ - Return an SVG image instead of PNG?  Exclusive with `retina`.
* `retina` - _optional_ - Return a larger image suitable for retina displays?  Exclusive with `svg`.
* `passingText` - _optional_ - Text to show in badge when build is passing.
* `failingText` - _optional_ - Text to show in badge when build is failing.
* `pendingText` - _optional_ - Text to show in badge when build is pending.

### Get project branch status badge image

*Tags:* `Project`

#### Input Parameters
* `svg` - _optional_ - Return an SVG image instead of PNG?  Exclusive with `retina`.
* `retina` - _optional_ - Return a larger image suitable for retina displays?  Exclusive with `svg`.
* `passingText` - _optional_ - Text to show in badge when build is passing.
* `failingText` - _optional_ - Text to show in badge when build is failing.
* `pendingText` - _optional_ - Text to show in badge when build is pending.

### Delete project

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Get project last build

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Get last successful build artifact

> The `job` parameter is mandatory if the build contains multiple jobs.

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug
* `artifactFileName` - _required_ - File name (or path) of a build artifact file.
Corresponds to the `fileName` property of `ArtifactModel`.
URL-encoding of slashes in parameter values is optional.
* `branch` - _optional_ - Repository Branch
* `tag` - _optional_ - A git (or other VCS) tag
* `job` - _optional_ - Name of the build job.
* `all` - _optional_ - Include not only `successful`, but also jobs with `failed`, and
`cancelled` status.
* `pr` - _optional_ - Include PR builds in the search results?
`true` - take artifact from PR builds only;
`false` - do not look for artifact in PR builds;
default/unspecified - look for artifact in both PR an non-PR builds.


### Get project last branch build

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug
* `buildBranch` - _required_ - Build Branch

### Get project build by version

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug
* `buildVersion` - _required_ - Build Version (`version` property of `Build`)

### Delete project build cache

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Get project deployments

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug
* `recordsNumber` - _required_ - Number of results to include in the response. getProjectDeployments is documented to have a maximum of 20. It currently returns 500 Internal Server Error for recordsNumber <= 5. In the past it has returned 500 Internal Server Error for many different values which did not match the value used by the ci.appveyor.com web interface at the time.  As of 2018-09-08, the value used by the web interface is 10.

### Get project history

*Tags:* `Project`

#### Input Parameters
* `recordsNumber` - _required_ - Number of results to include in the response. getProjectDeployments is documented to have a maximum of 20. It currently returns 500 Internal Server Error for recordsNumber <= 5. In the past it has returned 500 Internal Server Error for many different values which did not match the value used by the ci.appveyor.com web interface at the time.  As of 2018-09-08, the value used by the web interface is 10.
* `startBuildId` - _optional_ - Maximum `buildId` to include in the results (exclusive).
* `branch` - _optional_ - Repository Branch

### Get project settings

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Update project build number

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Get project environment variables

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Update project environment variables

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Get project settings in YAML

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Update project settings in YAML

*Tags:* `Project`

#### Input Parameters
* `accountName` - _required_ - AppVeyor account name (`accountName` property of `UserAccount`)
* `projectSlug` - _required_ - Project Slug

### Get roles

*Tags:* `Role`

### Add role

*Tags:* `Role`

### Update role

*Tags:* `Role`

### Delete role

*Tags:* `Role`

#### Input Parameters
* `roleId` - _required_ - Role ID

### Get role

*Tags:* `Role`

#### Input Parameters
* `roleId` - _required_ - Role ID

### Get users

*Tags:* `User`

### Add user

*Tags:* `User`

### Update user

*Tags:* `User`

### Delete user

*Tags:* `User`

#### Input Parameters
* `userId` - _required_ - User ID

### Get user

*Tags:* `User`

#### Input Parameters
* `userId` - _required_ - User ID

## License

flowground :- Telekom iPaaS / appveyor-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
