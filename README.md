# digipath-docs

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
