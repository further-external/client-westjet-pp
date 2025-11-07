# CTA Link Clicked

### 

## Javascript Code
```js
window.digitalEventData = window.digitalEventData || [];
digitalEventData.push({
  "event": "CTA Link Clicked",
    "linkInfo": {
        "linkId": "<linkId>"
    },
    "page": {
        "pageName": "<pageName>"
    },
    "westJetData": {
        "pageURL": "<pageURL>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|linkInfo.linkId|string|Identifier of the link clicked|act now, cancel, ok, 3456, 8765|||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||
|westJetData.pageURL|string|Captures the URL of the page.||||||||




