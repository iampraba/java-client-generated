# ShowEditorApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**previewPresentation**](ShowEditorApi.md#previewPresentation) | **POST** /show/officeapi/v1/spreadsheet/preview | 

<a name="previewPresentation"></a>
# **previewPresentation**
> PreviewResponse previewPresentation(document, url, language)



To open a presentation in preview or read-only mode in Zoho Sheet.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.ShowEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

ShowEditorApi apiInstance = new ShowEditorApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
String language = "language_example"; // String | 
try {
    PreviewResponse result = apiInstance.previewPresentation(document, url, language);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling ShowEditorApi#previewPresentation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **language** | **String**|  | [optional] [enum: da, de, es, fr, hu, it, ja, nl, pl, pt, ru, sv, tr, zh, zh_CN, vi, cs, el, et, fi, hr, ko, lt, sk, th, uk, bg, ca, false, ro, ar, iw, ur]

### Return type

[**PreviewResponse**](PreviewResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

