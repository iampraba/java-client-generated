# WriterCallbackSettings

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**saveUrl** | **String** | Provide your server location to which the latest content needs to be pushed back when the &#x27;Save&#x27; is performed. |  [optional]
**saveFormat** | [**WriterSupportedFormats**](WriterSupportedFormats.md) |  | 
**httpMethodType** | [**HttpMethodTypeEnum**](#HttpMethodTypeEnum) | Specify the http method in which the save request has to be triggered. |  [optional]
**retries** | **Integer** | Specify the number of retries required when the &#x27;Save&#x27; fails. |  [optional]
**timeout** | **Integer** | Specify the timeout for the given saveurl. |  [optional]
**saveUrlParams** | **Map&lt;String, Object&gt;** | To customize the output parameters in which the document details will be pushed from our end. |  [optional]

<a name="HttpMethodTypeEnum"></a>
## Enum: HttpMethodTypeEnum
Name | Value
---- | -----
POST | &quot;post&quot;
PUT | &quot;put&quot;
