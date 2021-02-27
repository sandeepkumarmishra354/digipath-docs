# digipath-docs Admin

### Get user list

`GET /api/v1/admin/user`
response

```json
[
   {
      "id":"unique uuid",
      "createdAt":"2021-02-27T06:30:35.509Z",
      "updatedAt":"2021-02-27T06:30:35.509Z",
      "firstName":"first name",
      "lastName":"last name",
      "email":"address@email.com",
      "contactNumber":"1234567890",
      "contactNumberOp":"1234567890",
      "departmentName":"department",
      "departmentId":"unique uuid",
      "designation":"designation",
      "photo":"photo url"
   }
]
```

### Get single user info

`GET /api/v1/admin/user/:userId`\
userId = "user's unique uuid"
response

```json
{
   "id":"unique uuid",
   "createdAt":"2021-02-27T06:30:35.509Z",
   "updatedAt":"2021-02-27T06:30:35.509Z",
   "firstName":"first name",
   "lastName":"last name",
   "email":"address@email.com",
   "contactNumber":"1234567890",
   "contactNumberOp":"1234567890",
   "departmentName":"department",
   "departmentId":"unique uuid",
   "designation":"designation",
   "photo":"photo url"
}
```

### Get department list

`GET /api/v1/admin/master/departments`
response

```json
[
   {
      "id":"unique uuid",
      "name":"department name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

### Create department

`POST /api/v1/admin/master/departments`
request data

```json
[
   {
      "name":"department name",
      "description":"this is description"
   }
]
```

response data

```json
[
   {
      "id":"unique uuid",
      "name":"department name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

### Update department

`PUT /api/v1/admin/master/departments`
request data

```json
[
   {
      "id":"department uuid",
      "name":"department name",
      "description":"this is description"
   }
]
```

response data

```json
[
   {
      "id":"unique uuid",
      "name":"department name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```


### Get scheme list

`GET /api/v1/admin/master/schemes`
response

```json
[
   {
      "id":"unique uuid",
      "name":"scheme name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

### Create scheme

`POST /api/v1/admin/master/schemes`
request data

```json
[
   {
      "name":"scheme name",
      "description":"this is description"
   }
]
```

response data

```json
[
   {
      "id":"unique uuid",
      "name":"scheme name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

### Update scheme

`PUT /api/v1/admin/master/schemes`
request data

```json
[
   {
      "id":"scheme uuid",
      "name":"scheme name",
      "description":"this is description"
   }
]
```

response data

```json
[
   {
      "id":"unique uuid",
      "name":"scheme name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

### Get field inspection

`GET /api/v1/admin/master/field-inspection`
response

```json
[
   {
      "id":"unique uuid",
      "userId":"user's uuid",
      "createdAt":"2021-02-27T06:30:35.509Z",
      "updatedAt":"2021-02-27T06:30:35.509Z",
      "departmentName":"department name",
      "departmentId":"department uuid",
      "schemeName":"scheme name",
      "schemeId":"scheme uuid",
      "areaType":"rural || urban",
      "areaId":"area uuid",
      "remarks":"this is remark",
      "placeName":"place name",
      "lat":21.343434,
      "lng":73.563454,
      "photos":[
         "url 1",
         "url 2",
         "url 3"
      ],
      "userFullName":"full name of user"
   }
]
```

### Update field inspection

`PUT /api/v1/admin/master/field-inspection`
response

```json
[
   {
      "id":"unique uuid",
      "department":"department uuid",
      "scheme":"scheme uuid",
      "areaType":"rural || urban",
      "areaId":"area uuid",
      "remarks":"this is remark",
      "placeName":"place name",
      "lat":21.343434,
      "lng":73.563454,
      "photos":[
         "url 1",
         "url 2",
         "url 3"
      ]
   }
]
```

### Get area list (rural || urban)

`GET /api/v1/admin/master/area/rural`
response

```json
[
   {
      "id":"unique uuid",
      "createdAt":"2021-02-27T06:30:35.509Z",
      "updatedAt":"2021-02-27T06:30:35.509Z",
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```

`GET /api/v1/admin/master/area/urban`
response

```json
[
   {
      "id":"unique uuid",
      "createdAt":"2021-02-27T06:30:35.509Z",
      "updatedAt":"2021-02-27T06:30:35.509Z",
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```

### Create area list (rural || urban)

`POST /api/v1/admin/master/area/rural`
response

```json
[
   {
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```

`POST /api/v1/admin/master/area/urban`
response

```json
[
   {
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```


### Update area list (rural || urban)

`PUT /api/v1/admin/master/area/rural`
response

```json
[
   {
      "id":"unique uuid",
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```

`PUT /api/v1/admin/master/area/urban`
response

```json
[
   {
      "id":"unique uuid",
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```

# digipath-docs Mobile App

#### Authentication

`POST /api/v1/public/auth/register`
request data

```json
{
    "firstName": "first name",
    "lastName": "last name",
    "contactNumber": "1234567890",
    "contactNumberOp": "optional",
    "department": "department uuid",
    "designation": "employee",
    "email": "address@email.com"
}
```

response data

```json
{
   "id": "unique uuid",
   "createdAt": "2021-02-27T06:30:35.509Z"
}
```

`POST /api/v1/public/auth/send-otp?phone=1234567890`
send phone as query parameter

response data

```json
{
   "otpToken": "otp session token",
   "status": "pending || verified || expired",
   "phone": "1234567890",
   "requestId": "sms request id"
}
```
otpToken is important in order to verify and resend the otp.

`POST /api/v1/public/auth/verify-otp?phone=1234567890&token=otpsessiontoken`
send phone & token as query parameter

response data

```json
{
   "status": "pending || verified || expired",
   "otpToken": "otp session token",
   "sessionToken": "unique session token"
}
```
if verification success a session token returned, save that token it will be required for subsequent requests.

`POST /api/v1/public/auth/resend-otp?token=otpsessiontoken`
send token as query parameter

response data

```json
{
   "otpToken": "otp session token",
   "status": "pending || verified || expired",
}
```

`POST /api/v1/public/auth/logout`
send sessionToken as request header ex- header["sessiontoken"] = "secret-token"

response data status = 200

```json
{ }
```

#### Field inspection

`POST /api/v1/public/field-inspection`
send sessionToken as request header ex- header["sessiontoken"] = "secret-token"

request data

```json
[
   {
      "department": "department uuid",
      "scheme": "scheme uuid",
      "remarks": "this is my remark",
      "placeName": "place name",
      "latitude": 12.324321,
      "longitude": 73.56442,
      "areaId": "area uuid",
      "areaType": "rural || urban",
      "photo": ["url 1", "url 2", "url 3"]
   }
]
```

response data

```json
[
   {
      "id": "unique uuid",
      "createdAt": "2021-02-27T06:30:35.509Z",
      "departmentName": "department name",
      "departmentId": "department uuid",
      "schemeName": "scheme name",
      "schemeId": "scheme uuid",
      "placeName": "place name",
      "lat": 12.345545,
      "lng": 82.54534,
      "remarks": "this is remark",
      "areaType": "rural || urban",
      "areaId": "area uuid",
      "userId": "user uuid",
      "userFullName": "firstname lastname",
      "photo": ["url 1", "url 2", "url 3"]
   }
]
```


#### Scheme - Department - Area

`POST /api/v1/public/misc/schemes`
send sessionToken as request header ex- header["sessiontoken"] = "secret-token"

request data

```json
[
   {
      "name":"scheme name",
      "description":"this is description"
   }
]
```

response data

```json
[
   {
      "id":"unique uuid",
      "name":"scheme name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

`GET /api/v1/public/misc/departments`
response

```json
[
   {
      "id":"unique uuid",
      "name":"department name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

`GET /api/v1/public/misc/schemes`
response

```json
[
   {
      "id":"unique uuid",
      "name":"scheme name",
      "description":"this is description",
      "createdAt":"2021-02-27T06:30:35.509Z"
   }
]
```

`GET /api/v1/public/misc/areas?type=rural||urban`
query parameter type = rural or urban only one at a time

response

```json
[
   {
      "id":"unique uuid",
      "createdAt":"2021-02-27T06:30:35.509Z",
      "updatedAt":"2021-02-27T06:30:35.509Z",
      "tehsilName":"name of tehsil",
      "blockName":"name of block",
      "gramSabha":"gram sabha name",
      "bhulekhNumber":123,
      "census01Code":43,
      "revenueVillName":"rajaswa gram name",
      "relatedStation":"sambandhit thana",
      "relatedAssembly":"sambandhit vidhan sabha"
   }
]
```


# Delete rows

#### to delete any above data just send ``DELETE`` request with query parameter ``?id=asesad,qewesad,wq3sdc`` id must be seperated by comma if there is multiple deletion.

Example
`DELETE /api/v1/admin/master/departments?id=wsdwsaw,swerw3sd,sdwrdf`

# NOTE

#### Every response object format is-

```json
{
    "status": 200,
    "message": "message related to success or error",
    "payload": {}
}
```

status is HTTP STATUS CODES ex- 200, 400, 404, 501 etc

payload can be json object or array of json object (depends on request)

#### Example

`GET /api/v1/admin/master/area/urban`


```json
{
    "status": 200,
    "message": "success",
    "payload": {
        "id":"unique uuid",
        "createdAt":"2021-02-27T06:30:35.509Z",
        "updatedAt":"2021-02-27T06:30:35.509Z",
        "tehsilName":"name of tehsil",
        "blockName":"name of block",
        "gramSabha":"gram sabha name",
        "bhulekhNumber":123,
        "census01Code":43,
        "revenueVillName":"rajaswa gram name",
        "relatedStation":"sambandhit thana",
        "relatedAssembly":"sambandhit vidhan sabha"
    }
}
```
