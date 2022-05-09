---
description: >-
  Fetching: - admin's user details, list of departments, locations, and users. 
  Post Create / Update User, Department, and Location.
---

# Admin

### Fetching

#### General Information or details

{% swagger baseUrl="https://localhost:3000" method="get" path="/api/info" summary="Return a list of  objects:" %}
{% swagger-description %}
departments?: object\[]&#x20;

locations?: object\[]&#x20;

orderTypes?: object\[]&#x20;

quantity\_unit?: string\[]&#x20;

order\_status?: string\[]&#x20;

item\_size?: string\[]&#x20;

message: string&#x20;

error?: boolean
{% endswagger-description %}

{% swagger-response status="200" description="Info fetched successfully" %}
```javascript
{
   "departments":[
      {
         "id":5,
         "name":"Arts & Humanities"
      },
      {
         "id":4,
         "name":"Business Administration"
      },
      {
         "id":3,
         "name":"Education"
      },

   ],
   "locations":[
      {
         "id":1,
         "building":"Information_Technology",
         "floor":1,
         "room_number":"101",
         "description":null,
         "total_quantity":0,
         "update_date":"2022-05-08T06:13:50.630Z",
         "short_code":"IT101",
         "department_id":null
      },
      {
         "id":2,
         "building":"Information_Technology",
         "floor":1,
         "room_number":"102",
         "description":null,
         "total_quantity":0,
         "update_date":"2022-05-08T06:13:50.630Z",
         "short_code":"IT102",
         "department_id":null
      },
    
         "id":15,
         "building":"Administration",
         "floor":1,
         "room_number":"102",
         "description":null,
         "total_quantity":0,
         "update_date":"2022-05-08T06:13:50.630Z",
         "short_code":"AD102",
         "department_id":null
      },
      {
         "id":16,
         "building":"Administration",
         "floor":1,
         "room_number":"103",
         "description":null,
         "total_quantity":0,
         "update_date":"2022-05-08T06:13:50.630Z",
         "short_code":"AD103",
         "department_id":null
      },
      {
         "id":17,
         "building":"Administration",
         "floor":1,
         "room_number":"104",
         "description":null,
         "total_quantity":0,
         "update_date":"2022-05-08T06:13:50.630Z",
         "short_code":"AD104",
         "department_id":null
      },
   
   ],
   "orderTypes":[
      
   ],
   "order_status":[
      "Pending",
      "Approved",
      "Purchased",
      "Rejected"
   ],
   "item_size":[
      "small",
      "medium",
      "large",
      "extra_large",
      "other"
   ],
   "quantity_unit":[
      "kilogram",
      "gram",
      "inches",
      "meter",
      "pound",
      "litre",
      "square_meter",
      "cubic_meter",
      "other quantity"
   ]
}
```


{% endswagger-response %}

{% swagger-response status="401" description="Permission denied" %}

{% endswagger-response %}
{% endswagger %}

{% hint style="info" %}
**Good to know:** This API method was created using the API Method block, it's how you can build out an API method documentation from scratch. Have a play with the block and you'll see you can do some nifty things like add and reorder parameters, document responses, and give your methods detailed descriptions.
{% endhint %}

## Department

#### Create Department { name, dean\_email }

#### Update Department { name, dean\_email }

### Location

#### Create Location { building: A?, floor: #, room\_number: A, description: A? }

#### &#x20;Update Location { building: A?, floor: #, room\_number: A, description: A? }
