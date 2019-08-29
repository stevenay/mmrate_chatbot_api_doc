# Create Schedule

ယခု Api Endpoint မှာ BP MMRate System မှ DigitX Chatbot Platform သို့ ခေါ်ရန် ဖြစ်ပါသည်။

Chatbot Users များသို့ Updated စျေးနှုန်းများ ပို့ရန်အတွက် Schedule ပြုလုပ်ခြင်း ဖြစ်ပါသည်။

Api Call တစ်ခုတွင် Exchange Rate, Oil Price, Gold Price အပြည့်အစုံ ပါဝင်ရမည် ဖြစ်ပါသည်။  currency_name, gold_market, oil_shop, oil_type စသည့် String Value များမှာ ကြိုတင် သဘောတူညီထားသော String များသာ ဖြစ်ရပါမည်။

**URL** : `/api/schedules/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : None

**Data constraints**

အောက်ပါ အချက်အလက်များကို Json Format ဖြင့် Post Request တွင် ထည့်သွင်းပေးရမည် ဖြစ်ပါသည်။

```json
  
{  
"exchange_rate": [  
{  
"currency_name": "USD",  
"buy_price": 1600,  
"sale_price": 1650  
},  
{  
"currency_name": "SGD",  
"buy_price": 1600,  
"sale_price": 1650  
}  
],  
"gold_price": [  
{  
"gold_market": "YGN",  
"gold_quality": "16(optional)",  
"gold_price": 11000000  
},  
{  
"gold_market": "MDY",  
"gold_quality": "16(optional)",  
"gold_price": 11000000  
}  
],  
"oil_price": [  
{  
"oil_shop": "DENKO",  
"oil_type": "DISEL",  
"oil_price": 950  
},  
{  
"oil_shop": "DENKO",  
"oil_type": "OCTANE 95",  
"oil_price": 960  
}  
],  
"broadcast_information": {  
"release_time_date": "2019-08-28 19:00:00",  
"sender": "BP(optional)"  
},  
"service_status": {  
"is_exchange_rate_update": false,  
"is_gold_price_update": false,  
"is_oil_price_update": false  
}  
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
eyJoaXN0b3J5IjpbMTIwNjYxMDM2M119
-->