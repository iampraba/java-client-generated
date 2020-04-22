# MailMergeWebHookSettings

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invokeUrl** | **String** | Provide the webhook url in which the merged documents needs to be posted. |  [optional]
**invokePeriod** | [**InvokePeriodEnum**](#InvokePeriodEnum) | when the merged documents needs to be posted in invoke_period. |  [optional]

<a name="InvokePeriodEnum"></a>
## Enum: InvokePeriodEnum
Name | Value
---- | -----
ONCOMPLETE | &quot;oncomplete&quot;
ONEVERYRECORD | &quot;oneveryrecord&quot;
