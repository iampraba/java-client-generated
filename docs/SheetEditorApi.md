# SheetEditorApi

All URIs are relative to *https://api.office-integrator.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createPresentation**](SheetEditorApi.md#createPresentation) | **POST** /show/officeapi/v1/presentation | 
[**createSpreadsheet**](SheetEditorApi.md#createSpreadsheet) | **POST** /sheet/officeapi/v1/spreadsheet | 
[**deleteSheet**](SheetEditorApi.md#deleteSheet) | **DELETE** /sheet/officeapi/v1/spreadsheet/{document_id} | 
[**deleteSheetSession**](SheetEditorApi.md#deleteSheetSession) | **DELETE** /sheet/officeapi/v1/session/{session_id} | 
[**deleteShow**](SheetEditorApi.md#deleteShow) | **DELETE** /show/officeapi/v1/presentation/{document_id} | 
[**deleteShowSession**](SheetEditorApi.md#deleteShowSession) | **DELETE** /show/officeapi/v1/session/{session_id} | 
[**previewSpreadsheet**](SheetEditorApi.md#previewSpreadsheet) | **POST** /sheet/officeapi/v1/spreadsheet/preview | 

<a name="createPresentation"></a>
# **createPresentation**
> CreateDocumentResponse createPresentation(document, url, callbackSettings, editorSettings, permissions, documentInfo, userInfo)



To create/edit a presentation in Zoho Show.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
ShowCallbackSettings callbackSettings = new ShowCallbackSettings(); // ShowCallbackSettings | 
Showofficeapiv1presentationEditorSettings editorSettings = new Showofficeapiv1presentationEditorSettings(); // Showofficeapiv1presentationEditorSettings | 
SheetEditPermissions permissions = new SheetEditPermissions(); // SheetEditPermissions | 
DocumentInfo documentInfo = new DocumentInfo(); // DocumentInfo | 
UserInfo userInfo = new UserInfo(); // UserInfo | 
try {
    CreateDocumentResponse result = apiInstance.createPresentation(document, url, callbackSettings, editorSettings, permissions, documentInfo, userInfo);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#createPresentation");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **callbackSettings** | [**ShowCallbackSettings**](.md)|  | [optional]
 **editorSettings** | [**Showofficeapiv1presentationEditorSettings**](.md)|  | [optional]
 **permissions** | [**SheetEditPermissions**](.md)|  | [optional]
 **documentInfo** | [**DocumentInfo**](.md)|  | [optional]
 **userInfo** | [**UserInfo**](.md)|  | [optional]

### Return type

[**CreateDocumentResponse**](CreateDocumentResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="createSpreadsheet"></a>
# **createSpreadsheet**
> CreateSheetResponse createSpreadsheet(document, url, callbackSettings, editorSettings, permissions, documentInfo, userInfo)



To create a new document in Zoho Writer.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
SheetCallbackSettings callbackSettings = new SheetCallbackSettings(); // SheetCallbackSettings | 
SheetEditorSettings editorSettings = new SheetEditorSettings(); // SheetEditorSettings | 
SheetEditPermissions permissions = new SheetEditPermissions(); // SheetEditPermissions | 
DocumentInfo documentInfo = new DocumentInfo(); // DocumentInfo | 
SheetUserInfo userInfo = new SheetUserInfo(); // SheetUserInfo | 
try {
    CreateSheetResponse result = apiInstance.createSpreadsheet(document, url, callbackSettings, editorSettings, permissions, documentInfo, userInfo);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#createSpreadsheet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **callbackSettings** | [**SheetCallbackSettings**](.md)|  | [optional]
 **editorSettings** | [**SheetEditorSettings**](.md)|  | [optional]
 **permissions** | [**SheetEditPermissions**](.md)|  | [optional]
 **documentInfo** | [**DocumentInfo**](.md)|  | [optional]
 **userInfo** | [**SheetUserInfo**](.md)|  | [optional]

### Return type

[**CreateSheetResponse**](CreateSheetResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

<a name="deleteSheet"></a>
# **deleteSheet**
> InlineResponse2001 deleteSheet(documentId)



To delete a particular document in Zoho Writer through a unique document id.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
String documentId = "documentId_example"; // String | Unique id of the document to be deleted.
try {
    InlineResponse2001 result = apiInstance.deleteSheet(documentId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#deleteSheet");
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

<a name="deleteSheetSession"></a>
# **deleteSheetSession**
> InlineResponse200 deleteSheetSession(sessionId)



To delete a particular user session of in Zoho Sheet.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
String sessionId = "sessionId_example"; // String | Unique user session id of the sheet document.
try {
    InlineResponse200 result = apiInstance.deleteSheetSession(sessionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#deleteSheetSession");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sessionId** | **String**| Unique user session id of the sheet document. |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="deleteShow"></a>
# **deleteShow**
> InlineResponse2002 deleteShow(documentId)



To delete a particular presentation in Zoho Show through a unique document id.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
String documentId = "documentId_example"; // String | Unique id of the presentation to be deleted.
try {
    InlineResponse2002 result = apiInstance.deleteShow(documentId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#deleteShow");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **documentId** | **String**| Unique id of the presentation to be deleted. |

### Return type

[**InlineResponse2002**](InlineResponse2002.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="deleteShowSession"></a>
# **deleteShowSession**
> InlineResponse200 deleteShowSession(sessionId)



To delete a particular user session of in Zoho Show.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
String sessionId = "sessionId_example"; // String | Unique user session id of the presentation.
try {
    InlineResponse200 result = apiInstance.deleteShowSession(sessionId);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#deleteShowSession");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **sessionId** | **String**| Unique user session id of the presentation. |

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="previewSpreadsheet"></a>
# **previewSpreadsheet**
> PreviewSheetResponse previewSpreadsheet(document, url, language, permissions)



To open a spreadsheet in preview or read-only mode in Zoho Sheet.

### Example
```java
// Import classes:
//import com.officeintegrator.ApiClient;
//import com.officeintegrator.ApiException;
//import com.officeintegrator.Configuration;
//import com.officeintegrator.auth.*;
//import com.officeintegrator.api.SheetEditorApi;

ApiClient defaultClient = Configuration.getDefaultApiClient();

// Configure API key authorization: apiKey
ApiKeyAuth apiKey = (ApiKeyAuth) defaultClient.getAuthentication("apiKey");
apiKey.setApiKey("YOUR API KEY");
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//apiKey.setApiKeyPrefix("Token");

SheetEditorApi apiInstance = new SheetEditorApi();
File document = new File("document_example"); // File | 
String url = "url_example"; // String | 
SheetSupportedLanguages language = new SheetSupportedLanguages(); // SheetSupportedLanguages | 
SheetReadOnlyPermissions permissions = new SheetReadOnlyPermissions(); // SheetReadOnlyPermissions | 
try {
    PreviewSheetResponse result = apiInstance.previewSpreadsheet(document, url, language, permissions);
    System.out.println(result);
} catch (ApiException e) {
    System.err.println("Exception when calling SheetEditorApi#previewSpreadsheet");
    e.printStackTrace();
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **document** | **File**|  | [optional]
 **url** | **String**|  | [optional]
 **language** | [**SheetSupportedLanguages**](.md)|  | [optional]
 **permissions** | [**SheetReadOnlyPermissions**](.md)|  | [optional]

### Return type

[**PreviewSheetResponse**](PreviewSheetResponse.md)

### Authorization

[apiKey](../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

