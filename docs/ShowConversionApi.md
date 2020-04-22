# ShowConversionApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convertPresentation**](ShowConversionApi.md#convertPresentation) | **POST** /show/officeapi/v1/presentation/convert | 

<a name="convertPresentation"></a>
# **convertPresentation**
> File convertPresentation(document, url, format)



To convert a document to any Show supported format (.pptx, .ppsx, .odf, .pdf)

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.ShowConversionApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

ShowConversionApi apiInstance = new ShowConversionApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
ShowExportFormats format = new ShowExportFormats(); // ShowExportFormats | 
try {
    File result = apiInstance.convertPresentation(document, url, format);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ShowConversionApi#convertPresentation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **format** | [**ShowExportFormats**](.md)|  | [optional]

### Return type

[**File**](File.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/_*, application/json

