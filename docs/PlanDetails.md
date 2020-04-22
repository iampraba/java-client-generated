# PlanDetails

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**apikeyId** | [**BigDecimal**](BigDecimal.md) | Unix id associted with apikey profile |  [optional]
**planName** | **String** | Current plan name |  [optional]
**paymentLink** | **String** | Link to make payment |  [optional]
**subscriptionInterval** | [**SubscriptionIntervalEnum**](#SubscriptionIntervalEnum) | Subscription billing cycle type. i.e - Yearly or Monthly |  [optional]
**subscriptionPeriod** | **String** | Subscription period string |  [optional]
**usageLimit** | **Integer** | Allowed api limit for current plan |  [optional]
**apikeyGeneratedTime** | **String** | Time when the apikey profile created |  [optional]
**totalUsage** | **Integer** | Total api usage count in this billing cycle |  [optional]
**remainingUsageLimit** | **Integer** | Remained allowed api limit |  [optional]
**lastPaymentDateMs** | [**BigDecimal**](BigDecimal.md) | Unix of last subscription payment date for Office Integrator service |  [optional]
**nextPaymentDateMs** | [**BigDecimal**](BigDecimal.md) | Unix of next subscription payment date for Office Integrator service |  [optional]
**lastPaymentDate** | **String** | Next payment date string value |  [optional]
**nextPaymentDate** | **String** | Next payment date string value |  [optional]

<a name="SubscriptionIntervalEnum"></a>
## Enum: SubscriptionIntervalEnum
Name | Value
---- | -----
YEARLY | &quot;yearly&quot;
MONTHLY | &quot;monthly&quot;
