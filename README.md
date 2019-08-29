# MMRate + DigitX Api Documentation

ယခု Api သည် MMRate CMS နှင့် DigitX Chatbot Platform တို့ကြား Integrate ပြုလုပ်ရန် ရည်ရွယ်ထားခြင်း ဖြစ်ပါသည်။

## Open Endpoints

Open endpoints require no Authentication.

## Endpoints with Authentication

အောက်ပါ Endpoints များကို access ပြုလုပ်ရန်အတွက် Api Key လိုအပ်ပါသည်။ Api Key ကို DigitX မှ ပံပိုးပေးပါမည်။


### Schedules

BP MMRate CMS မှ Exchange Rate, Oil Price, Gold Price စသည့် up-to-date price များကို Chatbot users များသို့ ပေးပို့ရန်အတွက် DigitX Platform သို့ Api ခေါ်၍ Schedule လုပ်ရန် Api ဖြစ်ပါသည်။

* [Create New Schedule](examples/schedules/post.md) : `POST /api/schedules/`
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTc0MTc3NjcxNiwyNDIyNzIxNjcsMTcwMD
U3MTY4M119
-->