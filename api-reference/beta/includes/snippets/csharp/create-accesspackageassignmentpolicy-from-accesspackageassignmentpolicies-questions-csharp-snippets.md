---
description: "Automatically generated file. DO NOT MODIFY"
---

```csharp

var graphClient = new GraphServiceClient(requestAdapter);

var requestBody = new AccessPackageAssignmentPolicy
{
	AccessPackageId = "b2eba9a1-b357-42ee-83a8-336522ed6cbf",
	DisplayName = "Users from connected organizations can request",
	Description = "Allow users from configured connected organizations to request and be approved by their sponsors",
	CanExtend = false,
	DurationInDays = 365,
	ExpirationDateTime = null,
	RequestorSettings = new RequestorSettings
	{
		ScopeType = "AllExistingConnectedOrganizationSubjects",
		AcceptRequests = true,
	},
	RequestApprovalSettings = new ApprovalSettings
	{
		IsApprovalRequired = true,
		IsApprovalRequiredForExtension = false,
		IsRequestorJustificationRequired = true,
		ApprovalMode = "SingleStage",
		ApprovalStages = new List<ApprovalStage>
		{
			new ApprovalStage
			{
				ApprovalStageTimeOutInDays = 14,
				IsApproverJustificationRequired = true,
				IsEscalationEnabled = false,
				EscalationTimeInMinutes = 11520,
				PrimaryApprovers = new List<UserSet>
				{
					new UserSet
					{
						OdataType = "#microsoft.graph.groupMembers",
						IsBackup = true,
						AdditionalData = new Dictionary<string, object>
						{
							{
								"id" , "d2dcb9a1-a445-42ee-83a8-476522ed6cbf"
							},
							{
								"description" , "group for users from connected organizations which have no external sponsor"
							},
						},
					},
					new UserSet
					{
						OdataType = "#microsoft.graph.externalSponsors",
						IsBackup = false,
					},
				},
			},
		},
	},
	Questions = new List<AccessPackageQuestion>
	{
		new AccessPackageQuestion
		{
			IsRequired = false,
			Text = new AccessPackageLocalizedContent
			{
				DefaultText = "what state are you from?",
				LocalizedTexts = new List<AccessPackageLocalizedText>
				{
					new AccessPackageLocalizedText
					{
						Text = "¿De qué estado eres?",
						LanguageCode = "es",
					},
				},
			},
			OdataType = "#microsoft.graph.accessPackageMultipleChoiceQuestion",
			AdditionalData = new Dictionary<string, object>
			{
				{
					"choices" , new List<>
					{
						new 
						{
							ActualValue = "AZ",
							DisplayValue = new 
							{
								LocalizedTexts = new List<>
								{
									new 
									{
										Text = "Arizona",
										LanguageCode = "es",
									},
								},
							},
						},
						new 
						{
							ActualValue = "CA",
							DisplayValue = new 
							{
								LocalizedTexts = new List<>
								{
									new 
									{
										Text = "California",
										LanguageCode = "es",
									},
								},
							},
						},
						new 
						{
							ActualValue = "OH",
							DisplayValue = new 
							{
								LocalizedTexts = new List<>
								{
									new 
									{
										Text = "Ohio",
										LanguageCode = "es",
									},
								},
							},
						},
					}
				},
				{
					"allowsMultipleSelection" , false
				},
			},
		},
		new AccessPackageQuestion
		{
			IsRequired = false,
			Text = new AccessPackageLocalizedContent
			{
				DefaultText = "Who is your manager?",
				LocalizedTexts = new List<AccessPackageLocalizedText>
				{
					new AccessPackageLocalizedText
					{
						Text = "por qué necesita acceso a este paquete",
						LanguageCode = "es",
					},
				},
			},
			OdataType = "#microsoft.graph.accessPackageTextInputQuestion",
			AdditionalData = new Dictionary<string, object>
			{
				{
					"isSingleLineQuestion" , false
				},
			},
		},
	},
};
var result = await graphClient.IdentityGovernance.EntitlementManagement.AccessPackageAssignmentPolicies.PostAsync(requestBody);


```