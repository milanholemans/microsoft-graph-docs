---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


requestId := "https://graph.microsoft.com/beta/groups/{other-group-id}"

requestParameters := &graphconfig.GroupItemAcceptedSenders$refRequestBuilderDeleteQueryParameters{
	Id: &requestId,
}
configuration := &graphconfig.GroupItemAcceptedSenders$refRequestBuilderDeleteRequestConfiguration{
	QueryParameters: requestParameters,
}

graphClient.GroupsById("group-id").AcceptedSenders().Ref().Delete(context.Background(), configuration)


```