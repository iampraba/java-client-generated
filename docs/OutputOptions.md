# OutputOptions

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | [**WriterSupportedFormats**](WriterSupportedFormats.md) |  | 
**documentName** | **String** | Specify the name for the converted document. | 
**password** | **String** | Specify a password if you would like to protect the converted document. |  [optional]
**includeChanges** | [**IncludeChangesEnum**](#IncludeChangesEnum) | Specify how the track changed content needs to be reflected in converted file. |  [optional]
**includeComments** | [**IncludeCommentsEnum**](#IncludeCommentsEnum) | Specify if the comments needs to be included in the converted file or not. |  [optional]

<a name="IncludeChangesEnum"></a>
## Enum: IncludeChangesEnum
Name | Value
---- | -----
AS_MARKUPS | &quot;as_markups&quot;
ALL | &quot;all&quot;
NONE | &quot;none&quot;

<a name="IncludeCommentsEnum"></a>
## Enum: IncludeCommentsEnum
Name | Value
---- | -----
ALL | &quot;all&quot;
NONE | &quot;none&quot;
