---
description: "Automatically generated file. DO NOT MODIFY"
---

```go

//THE GO SDK IS IN PREVIEW. NON-PRODUCTION USE ONLY
graphClient := msgraphsdk.NewGraphServiceClientWithCredentials(cred, scopes)

requestBody := graphmodels.NewUnifiedRoleManagementPolicyRule()
id := "Expiration_Admin_Assignment"
requestBody.SetId(&id) 
target := graphmodels.NewUnifiedRoleManagementPolicyRuleTarget()
caller := "Admin"
target.SetCaller(&caller) 
operations := []graphmodels.UnifiedRoleManagementPolicyRuleTargetOperationsable {
	unifiedRoleManagementPolicyRuleTargetOperations := graphmodels.ALL_UNIFIEDROLEMANAGEMENTPOLICYRULETARGETOPERATIONS 
	target.SetUnifiedRoleManagementPolicyRuleTargetOperations(&unifiedRoleManagementPolicyRuleTargetOperations) 

}
target.SetOperations(operations)
level := "Assignment"
target.SetLevel(&level) 
inheritableSettings := []string {

}
target.SetInheritableSettings(inheritableSettings)
enforcedSettings := []string {

}
target.SetEnforcedSettings(enforcedSettings)
requestBody.SetTarget(target)
additionalData := map[string]interface{}{
	isExpirationRequired := true
requestBody.SetIsExpirationRequired(&isExpirationRequired) 
	"maximumDuration" : "P90D", 
}
requestBody.SetAdditionalData(additionalData)

result, err := graphClient.Policies().RoleManagementPoliciesById("unifiedRoleManagementPolicy-id").RulesById("unifiedRoleManagementPolicyRule-id").Patch(context.Background(), requestBody, nil)


```