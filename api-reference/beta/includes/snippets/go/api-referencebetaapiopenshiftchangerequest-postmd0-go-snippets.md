---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

headers := abstractions.NewRequestHeaders()
headers.Add("Authorization", "Bearer {token}")

configuration := &graphconfig.TeamItemScheduleOpenShiftChangeRequestsRequestBuilderPostRequestConfiguration{
	Headers: headers,
}
requestBody := graphmodels.NewOpenShiftChangeRequest()
senderMessage := "Can I take this shift?"
requestBody.SetSenderMessage(&senderMessage) 
openShiftId := "577b75d2-a927-48c0-a5d1-dc984894e7b8"
requestBody.SetOpenShiftId(&openShiftId) 

result, err := graphClient.TeamsById("team-id").Schedule().OpenShiftChangeRequests().Post(context.Background(), requestBody, configuration)


```