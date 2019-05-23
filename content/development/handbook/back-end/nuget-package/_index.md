---
title: Nuget Package
description: Guidelines for error handling and error logging in backend
tags: ["nuget package", "create nuget", "back-end", "pre-release nuget"]
weight: 100
---
{{%notice warning%}}
This page is a work-in-progress. Because we do not have details on how potential errors should be shown to the users, this is only a general overview currently. More details will be added once we have a functional understanding of how users should experience errors. 
{{% /notice%}}

### Nuget Package

Altinn Studio publishes nuget package to share common libraries between different solutions. You can read more about nuget [here](https://www.nuget.org/).

Following nuget packages are published and are available for download [here] (https://www.nuget.org/profiles/altinn)

- [Altinn.Platform.Storage.Interface](https://www.nuget.org/packages/Altinn.Platform.Storage.Interface/)
- [AltinnCore.ServiceLibrary](https://www.nuget.org/packages/AltinnCore.ServiceLibrary/)
- [JWTCookieAuthentication](https://www.nuget.org/packages/JWTCookieAuthentication/)


### Create Nuget Package

Detailed documentation on how to create a nuget package, guidelines etc can be found [here](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio). 

### An example of  nuget package creation in altinn studio

Example : Create Altinn.Platform.Storage.Interface nuget package

### Set Project Properties

1. Open Altinn.Platform.Storage solution
2. Right click on Storage.Interface project and select properties. You will see the screen below
{{<figure src="storageinterface-props.png?width=1000" title="Project Properties">}}

3. Choose Package, add the package details such as id, version, description, author, company and tags.
4. Save the changes
5. Choose release mode
6. Right click on Storage.Interface and select "Pack"
7. The package will now be created in "C:\Repos\altinn-studio\src\Altinn.Platform\Altinn.Platform.Storage\Storage.Interface\bin\Release"
8. Go to commandline, navigate to the release path
9. run "dotnet nuget push Altinn.Platform.Storage.Interface.1.0.1-alpha.nupkg -k [nuget api key] -s https://api.nuget.org/v3/index.json"
10. Your package will now be published to nuget.org
