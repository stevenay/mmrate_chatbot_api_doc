# MMRate + DigitX Api Documentation

ယခု Api သည် MMRate CMS နှင့် DigitX Chatbot Platform တိုကြား Integrate ပြုလုပ်ရန် ရည်ရွယ်ထားခြင်း ဖြစ်ပါသည်။

## Open Endpoints

Open endpoints require no Authentication.

## Endpoints with Authentication

အောက်ပါ Endpoints များကို access ပြုလုပ်ရန်အတွက် Api Key လိုအပ်ပါသည်။ Api Key ကို DigitX မှ ပံပိုးပေးပါမည်။


### Schedules

Each endpoint manipulates or displays information related to the User whose
Token is provided with the request:

* [Show info](user/get.md) : `GET /api/user/`
* [Update info](user/put.md) : `PUT /api/user/`

### Account related

Endpoints for viewing and manipulating the Accounts that the Authenticated User
has permissions to access.

* [Show Accessible Accounts](accounts/get.md) : `GET /api/accounts/`
* [Create Account](accounts/post.md) : `POST /api/accounts/`
* [Show An Account](accounts/pk/get.md) : `GET /api/accounts/:pk/`
* [Update An Account](accounts/pk/put.md) : `PUT /api/accounts/:pk/`
* [Delete An Account](accounts/pk/delete.md) : `DELETE /api/accounts/:pk/`
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTc2Mzg4NTU3MV19
-->