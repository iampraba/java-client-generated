# WriterEditorApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**compareDocument**](WriterEditorApi.md#compareDocument) | **POST** /writer/officeapi/v1/document/compare | 
[**createDocument**](WriterEditorApi.md#createDocument) | **POST** /writer/officeapi/v1/document | 
[**deleteDocument**](WriterEditorApi.md#deleteDocument) | **DELETE** /writer/officeapi/v1/document/{document_id} | 
[**deleteWriterSession**](WriterEditorApi.md#deleteWriterSession) | **DELETE** /writer/officeapi/v1/session/{session_id} | 
[**previewDocument**](WriterEditorApi.md#previewDocument) | **POST** /writer/officeapi/v1/document/preview | 

<a name="compareDocument"></a>
# **compareDocument**
> CompareDocumentResponse compareDocument(document1, url1, document2, url2, title, lang)



To compare two versions of a document and highlight the difference in text.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterEditorApi apiInstance = new WriterEditorApi();
File document1 = new File("document1_example"); // File | 
String url1 = "url1_example"; // String | 
File document2 = new File("document2_example"); // File | 
String url2 = "url2_example"; // String | 
String title = "title_example"; // String | 
WriterSupportedLanguages lang = new WriterSupportedLanguages(); // WriterSupportedLanguages | 
try {
    CompareDocumentResponse result = apiInstance.compareDocument(document1, url1, document2, url2, title, lang);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterEditorApi#compareDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document1** | **File**|  | [optional]
 **url1** | **String**|  | [optional]
 **document2** | **File**|  | [optional]
 **url2** | **String**|  | [optional]
 **title** | **String**|  | [optional]
 **lang** | [**WriterSupportedLanguages**](.md)|  | [optional]

### Return type

[**CompareDocumentResponse**](CompareDocumentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="createDocument"></a>
# **createDocument**
> CreateDocumentResponse createDocument(document, url, callbackSettings, documentDefaults, editorSettings, permissions, documentInfo, userInfo, uiOptions)



To create a new document in Zoho Writer.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterEditorApi apiInstance = new WriterEditorApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
WriterCallbackSettings callbackSettings = new WriterCallbackSettings(); // WriterCallbackSettings | 
DocumentDefaults documentDefaults = new DocumentDefaults(); // DocumentDefaults | 
WriterEditorSettings editorSettings = new WriterEditorSettings(); // WriterEditorSettings | 
WriterPermissions permissions = new WriterPermissions(); // WriterPermissions | 
DocumentInfo documentInfo = new DocumentInfo(); // DocumentInfo | 
UserInfo userInfo = new UserInfo(); // UserInfo | 
UIOptions uiOptions = new UIOptions(); // UIOptions | 
try {
    CreateDocumentResponse result = apiInstance.createDocument(document, url, callbackSettings, documentDefaults, editorSettings, permissions, documentInfo, userInfo, uiOptions);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterEditorApi#createDocument");
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
 **uiOptions** | [**UIOptions**](.md)|  | [optional]

### Return type

[**CreateDocumentResponse**](CreateDocumentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="deleteDocument"></a>
# **deleteDocument**
> InlineResponse2001 deleteDocument(documentId)



To delete a particular document in Zoho Writer through a unique document id.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterEditorApi apiInstance = new WriterEditorApi();
String documentId = "documentId_example"; // String | Unique id of the document to be deleted.
try {
    InlineResponse2001 result = apiInstance.deleteDocument(documentId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterEditorApi#deleteDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **documentId** | **String**| Unique id of the document to be deleted. |

### Return type

[**InlineResponse2001**](InlineResponse2001.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="deleteWriterSession"></a>
# **deleteWriterSession**
> InlineResponse200 deleteWriterSession(sessionId)



To delete a user session of a particular document in Zoho Writer.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterEditorApi apiInstance = new WriterEditorApi();
String sessionId = "sessionId_example"; // String | Unique user session id of the document.
try {
    InlineResponse200 result = apiInstance.deleteWriterSession(sessionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterEditorApi#deleteWriterSession");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sessionId** | **String**| Unique user session id of the document. |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="previewDocument"></a>
# **previewDocument**
> PreviewResponse previewDocument(document, url, lang)



To create a new document in Zoho Writer.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.WriterEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

WriterEditorApi apiInstance = new WriterEditorApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
WriterSupportedLanguages lang = new WriterSupportedLanguages(); // WriterSupportedLanguages | 
try {
    PreviewResponse result = apiInstance.previewDocument(document, url, lang);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling WriterEditorApi#previewDocument");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **lang** | [**WriterSupportedLanguages**](.md)|  | [optional]

### Return type

[**PreviewResponse**](PreviewResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

