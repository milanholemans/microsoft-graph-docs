---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewDomain()
id := "contoso.com"
requestBody.SetId(&id) 

result, err := graphClient.Domains().Post(context.Background(), requestBody, nil)


```