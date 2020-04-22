# WriterMergeApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createDocumentTemplate**](WriterMergeApi.md#createDocumentTemplate) | **POST** /writer/officeapi/v1/template | 
[**getDocumentMergeFields**](WriterMergeApi.md#getDocumentMergeFields) | **POST** /writer/officeapi/v1/fields | 
[**mergeAndDeliverDocument**](WriterMergeApi.md#mergeAndDeliverDocument) | **POST** /writer/officeapi/v1/document/merge/webhook | 
[**mergeDocument**](WriterMergeApi.md#mergeDocument) | **POST** /writer/officeapi/v1/document/merge | 

<a name="createDocumentTemplate"></a>
# **createDocumentTemplate**
> CreateDocumentResponse createDocumentTemplate(document, url, callbackSettings, documentDefaults, editorSettings, permissions, documentInfo, userInfo, mergeDataCsvContent, mergeDataJsonContent)



To create a new template in Zoho Writer.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterMergeApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterMergeApi apiInstance = new WriterMergeApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
WriterCallbackSettings callbackSettings = new WriterCallbackSettings(); // WriterCallbackSettings | 
DocumentDefaults documentDefaults = new DocumentDefaults(); // DocumentDefaults | 
WriterEditorSettings editorSettings = new WriterEditorSettings(); // WriterEditorSettings | 
WriterPermissions permissions = new WriterPermissions(); // WriterPermissions | 
DocumentInfo documentInfo = new DocumentInfo(); // DocumentInfo | 
UserInfo userInfo = new UserInfo(); // UserInfo | 
File mergeDataCsvContent = new File("mergeDataCsvContent_example"); // File | 
File mergeDataJsonContent = new File("mergeDataJsonContent_example"); // File | 
try {
    CreateDocumentResponse result = apiInstance.createDocumentTemplate(document, url, callbackSettings, documentDefaults, editorSettings, permissions, documentInfo, userInfo, mergeDataCsvContent, mergeDataJsonContent);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterMergeApi#createDocumentTemplate");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **callbackSettings** | [**WriterCallbackSettings**](.md)|  | [optional]
 **documentDefaults** | [**DocumentDefaults**](.md)|  | [optional]
 **editorSettings** | [**WriterEditorSettings**](.md)|  | [optional]
 **permissions** | [**WriterPermissions**](.md)|  | [optional]
 **documentInfo** | [**DocumentInfo**](.md)|  | [optional]
 **userInfo** | [**UserInfo**](.md)|  | [optional]
 **mergeDataCsvContent** | **File**|  | [optional]
 **mergeDataJsonContent** | **File**|  | [optional]

### Return type

[**CreateDocumentResponse**](CreateDocumentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="getDocumentMergeFields"></a>
# **getDocumentMergeFields**
> GetMergeFieldsReponse getDocumentMergeFields(fileContent, fileUrl)



To get the list of available merge fields present in the document.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterMergeApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterMergeApi apiInstance = new WriterMergeApi();
File fileContent = new File("fileContent_example"); // File | 
String fileUrl = "fileUrl_example"; // String | 
try {
    GetMergeFieldsReponse result = apiInstance.getDocumentMergeFields(fileContent, fileUrl);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterMergeApi#getDocumentMergeFields");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileContent** | **File**|  | [optional]
 **fileUrl** | **String**|  | [optional]

### Return type

[**GetMergeFieldsReponse**](GetMergeFieldsReponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="mergeAndDeliverDocument"></a>
# **mergeAndDeliverDocument**
> MergeAndDeliverReponse mergeAndDeliverDocument(outputFormat, fileContent, fileUrl, webhook, mergeTo, mergeData, mergeDataCsvContent, mergeDataJsonContent, mergeDataCsvUrl, mergeDataJsonUrl, password)



To send or post the merged document to the given webhook URL.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterMergeApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterMergeApi apiInstance = new WriterMergeApi();
WriterMergeExportFormat outputFormat = new WriterMergeExportFormat(); // WriterMergeExportFormat | 
File fileContent = new File("fileContent_example"); // File | 
String fileUrl = "fileUrl_example"; // String | 
MailMergeWebHookSettings webhook = new MailMergeWebHookSettings(); // MailMergeWebHookSettings | 
String mergeTo = "mergeTo_example"; // String | 
Map<String, Object> mergeData = null; // Map<String, Object> | 
File mergeDataCsvContent = new File("mergeDataCsvContent_example"); // File | 
File mergeDataJsonContent = new File("mergeDataJsonContent_example"); // File | 
String mergeDataCsvUrl = "mergeDataCsvUrl_example"; // String | 
String mergeDataJsonUrl = "mergeDataJsonUrl_example"; // String | 
String password = "password_example"; // String | 
try {
    MergeAndDeliverReponse result = apiInstance.mergeAndDeliverDocument(outputFormat, fileContent, fileUrl, webhook, mergeTo, mergeData, mergeDataCsvContent, mergeDataJsonContent, mergeDataCsvUrl, mergeDataJsonUrl, password);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterMergeApi#mergeAndDeliverDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **outputFormat** | [**WriterMergeExportFormat**](.md)|  | [optional]
 **fileContent** | **File**|  | [optional]
 **fileUrl** | **String**|  | [optional]
 **webhook** | [**MailMergeWebHookSettings**](.md)|  | [optional]
 **mergeTo** | **String**|  | [optional] [enum: separatedoc, singledoc]
 **mergeData** | [**Map&lt;String, Object&gt;**](Object.md)|  | [optional]
 **mergeDataCsvContent** | **File**|  | [optional]
 **mergeDataJsonContent** | **File**|  | [optional]
 **mergeDataCsvUrl** | **String**|  | [optional]
 **mergeDataJsonUrl** | **String**|  | [optional]
 **password** | **String**|  | [optional]

### Return type

[**MergeAndDeliverReponse**](MergeAndDeliverReponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="mergeDocument"></a>
# **mergeDocument**
> File mergeDocument(outputFormat, fileContent, fileUrl, mergeData, mergeDataCsvContent, mergeDataJsonContent, mergeDataCsvUrl, mergeDataJsonUrl, password)



This API will allow you to generate documents and merge them.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterMergeApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterMergeApi apiInstance = new WriterMergeApi();
WriterMergeExportFormat outputFormat = new WriterMergeExportFormat(); // WriterMergeExportFormat | 
File fileContent = new File("fileContent_example"); // File | 
String fileUrl = "fileUrl_example"; // String | 
Map<String, Object> mergeData = null; // Map<String, Object> | 
File mergeDataCsvContent = new File("mergeDataCsvContent_example"); // File | 
File mergeDataJsonContent = new File("mergeDataJsonContent_example"); // File | 
String mergeDataCsvUrl = "mergeDataCsvUrl_example"; // String | 
String mergeDataJsonUrl = "mergeDataJsonUrl_example"; // String | 
String password = "password_example"; // String | 
try {
    File result = apiInstance.mergeDocument(outputFormat, fileContent, fileUrl, mergeData, mergeDataCsvContent, mergeDataJsonContent, mergeDataCsvUrl, mergeDataJsonUrl, password);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterMergeApi#mergeDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **outputFormat** | [**WriterMergeExportFormat**](.md)|  | [optional]
 **fileContent** | **File**|  | [optional]
 **fileUrl** | **String**|  | [optional]
 **mergeData** | [**Map&lt;String, Object&gt;**](Object.md)|  | [optional]
 **mergeDataCsvContent** | **File**|  | [optional]
 **mergeDataJsonContent** | **File**|  | [optional]
 **mergeDataCsvUrl** | **String**|  | [optional]
 **mergeDataJsonUrl** | **String**|  | [optional]
 **password** | **String**|  | [optional]

### Return type

[**File**](File.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/_*, application/json

