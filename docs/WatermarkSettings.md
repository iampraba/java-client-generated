# WatermarkSettings

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **String** | Specify the watermark content inside the &#x27;text&#x27; key | 
**type** | [**TypeEnum**](#TypeEnum) | Provide of watermark to be applied inside the &#x27;type&#x27; key. For now only type &#x27;text&#x27; only supported |  [optional]
**orientation** | [**OrientationEnum**](#OrientationEnum) | Orientation of watermark to be applied on the document |  [optional]
**fontName** | **String** | Font name in which the watermark text needs to be applied on the output document. |  [optional]
**fontSize** | **Integer** | Font size of the watermark text to be applied on the output document. Given size will be considered in inches. |  [optional]
**fontColor** | **String** | Font colour of the watermark text to be applied on the output document. Colours can be represented as &#x27;#04AB8F&#x27;. RGB format is also allowed. |  [optional]
**opacity** | **Integer** | Opacity value for watermark to be applied on the document |  [optional]

<a name="TypeEnum"></a>
## Enum: TypeEnum
Name | Value
---- | -----
TEXT | &quot;text&quot;

<a name="OrientationEnum"></a>
## Enum: OrientationEnum
Name | Value
---- | -----
DIAGONAL | &quot;diagonal&quot;
HORIZONTAL | &quot;horizontal&quot;
VERTICAL | &quot;vertical&quot;
