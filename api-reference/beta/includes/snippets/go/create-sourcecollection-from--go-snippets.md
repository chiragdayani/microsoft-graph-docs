---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClient(requestAdapter);

requestBody := msgraphsdk.NewSourceCollection()
displayName := "Quarterly Financials search"
requestBody.SetDisplayName(&displayName)
contentQuery := "subject:'Quarterly Financials'"
requestBody.SetContentQuery(&contentQuery)
requestBody.SetAdditionalData(map[string]interface{}{
	"custodianSources@odata.bind":  []String {
		"https://graph.microsoft.com/beta/compliance/ediscovery/cases/47746044-fd0b-4a30-acfc-5272b691ba5b/custodians/2192ca408ea2410eba3bec8ae873be6b/userSources/46384443-4137-3032-3437-363939433735",
	}
}
options := &msgraphsdk.SourceCollectionsRequestBuilderPostOptions{
	Body: requestBody,
}
caseId := "case-id"
result, err := graphClient.Compliance().Ediscovery().CasesById(&caseId).SourceCollections().Post(options)


```