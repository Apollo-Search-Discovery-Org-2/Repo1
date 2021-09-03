# User Visit Started

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "User Visit Started",
    "user": {
        "persistedCartValue": "<persistedCartValue>",
        "persistedcart": {
            "item": [
                {
                    "price": {
                        "sellingPrice": "<sellingPrice>"
                    },
                    "productInfo": {
                        "productID": "<productID>"
                    }
                }
            ]
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|persistedCartValue|string|The total value of all items in the persisted cart|125.05, 432.21, 90.22, 12.05|^[0-9]*(\.[0-9]{1,2})?$||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||



