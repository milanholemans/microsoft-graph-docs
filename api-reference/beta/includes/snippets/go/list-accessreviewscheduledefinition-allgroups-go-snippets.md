---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestFilter := "contains(scope/microsoft.graph.accessReviewQueryScope/query,%20'./members')"

requestParameters := &graphconfig.IdentityGovernanceAccessReviewsDefinitionsRequestBuilderGetQueryParameters{
	Filter: &requestFilter,
}
configuration := &graphconfig.IdentityGovernanceAccessReviewsDefinitionsRequestBuilderGetRequestConfiguration{
	QueryParameters: requestParameters,
}

result, err := graphClient.IdentityGovernance().AccessReviews().Definitions().Get(context.Background(), configuration)


```