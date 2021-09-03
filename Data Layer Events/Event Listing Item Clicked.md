# Event Listing Item Clicked

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Event Listing Item Clicked",
    "listingDisplayed": {
        "sortOrder": "<sortOrder>"
    },
    "listingItemClicked": {
        "filterList": "<filterList>",
        "listing": [
            {
                "event": {
                    "eventId": "<eventId>",
                    "eventName": "<eventName>",
                    "eventType": "<eventType>",
                    "status": "<status>"
                },
                "itemPosition": "<itemPosition>",
                "price": {
                    "currency": "<currency>"
                }
            }
        ]
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|currency|string|Currency of the prices given. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|eventId|string|Unique Identifier of an event. |155, 65588, 987764448|||||||
|eventName|string|The friendly name of the event.|Max your 401K, Structured JavaScript, Mid Day Yoga, Frosty 5K Fun Run, Whiskey Wednesday|||||||
|eventType|string|The type of the event|Webinar, Class, Conference, Race, Meet Up|||||||
|filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||
|itemPosition|integer|Integer position of a property within a sorted result. The first returned is position 1. For map results, this value can be the rank by distance from POI.|1, 2, 3, 4, 5||||0|||
|sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||
|status|string|The status of an event.|Cancelled, Sold Out, Postponed, Rescheduled|||||||



