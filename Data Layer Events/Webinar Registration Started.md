# Webinar Registration Started

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Webinar Registration Started",
    "webinar": {
        "webinarID": "<webinarID>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|webinarID|string|Unique identifier of the webinar for which a user is registering.  Should match back-end systems for upload of webinar meta data to enhance analysis.|TK-7869, GH-98657|||||||



