---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewReferenceCreate()
odataId := "https://graph.microsoft.com/v1.0/policies/claimsMappingPolicies/a4b35718-fd5e-4ca8-8248-a3c9934b1b78"
requestBody.SetOdataId(&odataId) 

graphClient.ServicePrincipalsById("servicePrincipal-id").ClaimsMappingPolicies().Ref().Post(context.Background(), requestBody, nil)


```