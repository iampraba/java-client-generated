# OfficeIntegratorApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPlanDetails**](OfficeIntegratorApi.md#getPlanDetails) | **GET** /api/v1/plan | 

<a name="getPlanDetails"></a>
# **getPlanDetails**
> PlanDetails getPlanDetails()



To retrieve the plan details including the API calls usage.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.OfficeIntegratorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

OfficeIntegratorApi apiInstance = new OfficeIntegratorApi();
try {
    PlanDetails result = apiInstance.getPlanDetails();
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling OfficeIntegratorApi#getPlanDetails");
    e.printStackTrace();
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PlanDetails**](PlanDetails.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

