---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)


result, err := graphClient.TenantRelationships().ManagedTenants().TenantGroupsById("tenantGroup-id").Get(context.Background(), nil)


```