---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewSet()
description := "mySet"
requestBody.SetDescription(&description) 

result, err := graphClient.SitesById("site-id").TermStore().SetsById("set-id").Patch(context.Background(), requestBody, nil)


```