# Create Schedule

ယခု Api Endpoint မှာ BP MMRate System မှ DigitX Chatbot Platform သို့ ခေါ်ရန် ဖြစ်ပါသည်။

Chatbot Users များသို့ Updated စျေးနှုန်းများ ပို့ရန်အတွက် Schedule ပြုလုပ်ခြင်း ဖြစ်ပါသည်။

Api Call တစ်ခုတွင် Exchange Rate, Oil Price, Gold Price အပြည့်အစုံ ပါဝင်ရမည် ဖြစ်ပါသည်။  currency_name, gold_market, oil_shop, oil_type စသည့် String Value များမှာ ကြိုတင် သဘောတူညီထားသော String များသာ ဖြစ်ရပါမည်။

**URL** : `/api/schedules/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : None

**Data constraints**

Provide name of Account to be created.

```json
{
    "name": "[unicode 64 chars max]"
}
```

**Data example** All fields must be sent.

```json
{
    "name": "Build something project dot com"
}
```

## Success Response

**Condition** : If everything is OK and an Account didn't exist for this User.

**Code** : `201 CREATED`

**Content example**

```json
{
    "id": 123,
    "name": "Build something project dot com",
    "url": "http://testserver/api/accounts/123/"
}
```

## Error Responses

**Condition** : If Account already exists for User.

**Code** : `303 SEE OTHER`

**Headers** : `Location: http://testserver/api/accounts/123/`

**Content** : `{}`

### Or

**Condition** : If fields are missed.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "name": [
        "This field is required."
    ]
}
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTEzOTExMDEwMTFdfQ==
-->