# digipath-docs

### Get single user list

``GET /api/v1/admin/user``</br>
response</br>
``[
{
id: "unique uuid",
createdAt: "2021-02-27T06:30:35.509Z",
updatedAt: "2021-02-27T06:30:35.509Z",
firstName: "first name",
lastName: "last name",
email: "address@email.com",
contactNumber: "1234567890",
contactNumberOp: "1234567890",//optional
departmentName: "department",
departmentId: "unique uuid",
designation: "designation",
photo: "photo url"
}
]``

### Get single user info



``GET /api/v1/admin/user/:userId``</br>
userId = "user's unique uuid"</br>
response</br>
``{
id: "unique uuid",
createdAt: "2021-02-27T06:30:35.509Z",
updatedAt: "2021-02-27T06:30:35.509Z",
firstName: "first name",
lastName: "last name",
email: "address@email.com",
contactNumber: "1234567890",
contactNumberOp: "1234567890",//optional
departmentName: "department",
departmentId: "unique uuid",
designation: "designation",
photo: "photo url"
}``

### Get department list

``GET /api/v1/admin/master/departments``</br>
response</br>
``[
{
id: "unique uuid",
name: "department name",
description: "this is description",//optional
createdAt: "2021-02-27T06:30:35.509Z"
}
]``

### Create department

``POST /api/v1/admin/master/departments``</br>
request data</br>
``[
{
name: "department name",
description: "this is description"
}
]``
response data</br>
``[
{
id: "unique uuid",
name: "department name",
description: "this is description",//optional
createdAt: "2021-02-27T06:30:35.509Z"
}
]``

### Update department

``PUT /api/v1/admin/master/departments``</br>
request data</br>
``[
{
id: "department uuid",
name: "department name",
description: "this is description"
}
]``
response data</br>
``[
{
id: "unique uuid",
name: "department name",
description: "this is description",//optional
createdAt: "2021-02-27T06:30:35.509Z"
}
]``


### Get scheme list

``GET /api/v1/admin/master/schemes``</br>
response</br>
``[
{
id: "unique uuid",
name: "scheme name",
description: "this is description",//optional
createdAt: "2021-02-27T06:30:35.509Z"
}
]``

### Create scheme

``POST /api/v1/admin/master/schemes``</br>
request data</br>
``[
{
name: "scheme name",
description: "this is description"
}
]``
response data</br>
``[
{
id: "unique uuid",
name: "scheme name",
description: "this is description",//optional
createdAt: "2021-02-27T06:30:35.509Z"
}
]``

### Update scheme

``PUT /api/v1/admin/master/schemes``</br>
request data</br>
``[
{
id: "scheme uuid",
name: "scheme name",
description: "this is description"
}
]``
response data</br>
``[
{
id: "unique uuid",
name: "scheme name",
description: "this is description",//optional
createdAt: "2021-02-27T06:30:35.509Z"
}
]``
