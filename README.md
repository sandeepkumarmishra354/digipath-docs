# digipath-docs

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


## Delete rows

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
