# Jenkins
[![Build status](https://ci.appveyor.com/api/projects/status/tp0scpm2rk0vej86/branch/master?svg=true)](https://ci.appveyor.com/project/IAG-NZ/jenkins/branch/master)

PowerShell module for interacting with a CloudBees Jenkins server using the [Jenkins Rest API](https://wiki.jenkins-ci.org/display/JENKINS/Remote+access+API) created by IAG NZ Ltd.

# Installation
> If Windows Management Framework 5.0 or above is installed or the PowerShell Package management module is available:

The easiest way to download and install the LabBuilder module is using PowerShell Get to download it from the PowerShell Gallery:
```powershell
Install-Module -Name Jenkins
```

> If Windows Management Framework 5.0 or above is not available and and the PowerShell Package management module is not available:

```
Unzip the file containing this Module to your c:\Program Files\WindowsPowerShell\Modules folder.
```

# Cmdlets
 - Invoke-JenkinsCommand: Execute a Jenkins command or request via the Jenkins Rest API.
 - Get-JenkinsObject: Get a list of objects in a Jenkins master server.
 - Get-JenkinsJobList: Get a list of jobs in a Jenkins master server.
 - Get-JenkinsJob: Get a Jenkins Job Definition.
 - Set-JenkinsJob: Set a Jenkins Job definition.
 - Test-JenkinsJob: Determines if a Jenkins Job exists.
 - New-JenkinsJob: Create a new Jenkins Job.
 - Remove-JenkinsJob: Remove an existing Jenkins Job.
 - Get-JenkinsViewList: Get a list of views in a Jenkins master server.
 - Test-JenkinsView: Determines if a Jenkins View exists.
 - Get-JenkinsFolderList: Get a list of folders in a Jenkins master server.
 - Test-JenkinsFolder: Determines if a Jenkins Folder exists.

# Future features
 - Add support for servers with Cross Site Request Forgery security optional enabled.

# Known Issues
 - Prevent Cross Site Request Forgery security option in Jenkins is not yet supported.
This feature will be added in a future release.
If you recieve errors regarding crumbs then your Jenkins Server has CSRF enabled and it will need to be disabled in the "Configure Global Security" section in Jenkins.
 - Remove-JenkinsJob: An IE window pops up after deleting the job for some reason requesting authentication.

# Recommendations
 - If your Jenkins Server has security enabled then you should ensure that you are only connecting to it via HTTPS.
 - If your Jenkins Server has security enabled, the Credentials parameter that can accept either the password for the Jenkins account or the API Token.
It is strongly recommended that you use the API Token for the account as the password rather than the Jenkins account, even if you have implemented HTTPS.

# Examples

# Versions

### Unreleased
* Initial Release containing:
  - Invoke-JenkinsCommand
  - Get-JenkinsObject
  - Get-JenkinsJobList
  - Get-JenkinsJob
  - Set-JenkinsJob
  - Test-JenkinsJob
  - New-JenkinsJob
  - Remove-JenkinsJob
  - Get-JenkinsViewList
  - Test-JenkinsView
  - Get-JenkinsFolderList
  - Test-JenkinsFolder

# Links
* [IAG NZ Web Site](http://www.iag.co.nz)
* [IAG NZ GitHub Organization](https://github.com/IAG-NZ)
* [Project site on GitHub](https://github.com/IAG-NZ/Jenkins)