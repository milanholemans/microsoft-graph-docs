---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

headers := abstractions.NewRequestHeaders()
headers.Add("ConsistencyLevel", "eventual")


requestFilter := "owners/$count eq 0 or owners/$count eq 1"
requestCount := true

requestParameters := &graphconfig.ServicePrincipalsRequestBuilderGetQueryParameters{
	Filter: &requestFilter,
	Count: &requestCount,
}
configuration := &graphconfig.ServicePrincipalsRequestBuilderGetRequestConfiguration{
	Headers: headers,
	QueryParameters: requestParameters,
}

result, err := graphClient.ServicePrincipals().Get(context.Background(), configuration)


```