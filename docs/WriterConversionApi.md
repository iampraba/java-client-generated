# WriterConversionApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convertDocument**](WriterConversionApi.md#convertDocument) | **POST** /writer/officeapi/v1/document/convert | 
[**watermarkDocument**](WriterConversionApi.md#watermarkDocument) | **POST** /writer/officeapi/v1/document/watermark | 

<a name="convertDocument"></a>
# **convertDocument**
> File convertDocument(document, url, outputOptions, password)



To convert a document to any Writer supported format (.docx, .doc, .pdf, .zdoc etc.)

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterConversionApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterConversionApi apiInstance = new WriterConversionApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
OutputOptions outputOptions = new OutputOptions(); // OutputOptions | 
String password = "password_example"; // String | 
try {
    File result = apiInstance.convertDocument(document, url, outputOptions, password);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterConversionApi#convertDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **outputOptions** | [**OutputOptions**](.md)|  | [optional]
 **password** | **String**|  | [optional]

### Return type

[**File**](File.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/_*, application/json

<a name="watermarkDocument"></a>
# **watermarkDocument**
> File watermarkDocument(document, url, watermarkSettings)



Using this API, you can provide the watermark details in the form of text.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterConversionApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterConversionApi apiInstance = new WriterConversionApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
WatermarkSettings watermarkSettings = new WatermarkSettings(); // WatermarkSettings | 
try {
    File result = apiInstance.watermarkDocument(document, url, watermarkSettings);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterConversionApi#watermarkDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **watermarkSettings** | [**WatermarkSettings**](.md)|  | [optional]

### Return type

[**File**](File.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/_*, application/json

