---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewReferenceCreate()
odataId := "https://graph.microsoft.com/v1.0/directoryObjects/2441b489-4f12-4882-b039-8f6006bd66da"
requestBody.SetOdataId(&odataId) 

graphClient.Policies().FeatureRolloutPoliciesById("featureRolloutPolicy-id").AppliesTo().Ref().Post(context.Background(), requestBody, nil)


```