---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


result, err := graphClient.Compliance().Ediscovery().CasesById("case-id").CustodiansById("custodian-id").UserSourcesById("userSource-id").Get(context.Background(), nil)


```