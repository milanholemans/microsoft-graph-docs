---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewCreateUploadSessionPostRequestBody()
attachmentInfo := graphmodels.NewAttachmentInfo()
attachmentType := graphmodels.FILE_ATTACHMENTTYPE 
attachmentInfo.SetAttachmentType(&attachmentType) 
name := "flower"
attachmentInfo.SetName(&name) 
size := int64(3483322)
attachmentInfo.SetSize(&size) 
requestBody.SetAttachmentInfo(attachmentInfo)

result, err := graphClient.Me().Todo().ListsById("todoTaskList-id").TasksById("todoTask-id").Attachments().CreateUploadSession().Post(context.Background(), requestBody, nil)


```