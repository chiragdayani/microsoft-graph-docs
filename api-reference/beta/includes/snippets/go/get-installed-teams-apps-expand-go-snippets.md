---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter);

requestParameters := &msgraphsdk.TeamsAppInstallationRequestBuilderGetQueryParameters{
	Expand: "teamsAppDefinition",
}
options := &msgraphsdk.TeamsAppInstallationRequestBuilderGetOptions{
	Q: requestParameters,
}
teamId := "team-id"
teamsAppInstallationId := "teamsAppInstallation-id"
result, err := graphClient.TeamsById(&teamId).InstalledAppsById(&teamsAppInstallationId).Get(options)


```