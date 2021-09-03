# Form Viewed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Viewed",
    "form": {
        "formField": [
            {
                "fieldID": "<fieldID>",
                "fieldPosition": "<fieldPosition>",
                "formSection": "<formSection>"
            }
        ],
        "formID": "<formID>",
        "formName": "<formName>",
        "formType": "<formType>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|fieldID|string|Unique identifier of a form field within a form. |first\_name, last\_name, addr\_line1, addr\_line2|||||||
|fieldPosition|integer|Integer position of a form field within a form.  The first for field is position 1.|1, 2, 3, 4, 5||||1|||
|formID|string|Unique identifier of a form. |F-0113, 2543, CU001, PI-0988|||||||
|formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|formSection|string|Describes the section of a form to which a form field belongs. Useful for reporting on complex forms.|address1, address2, cc info, terms acceptance|||||||
|formType|string|Form type used for grouping of similar forms in reports.  |Address, Contact, Comment, Review, Payment|||||||



