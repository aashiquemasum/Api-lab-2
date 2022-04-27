1. Send your first request:
Can you tell us in your own word what happened after making your first request?

Ans: I sent a get request to postman-echo.com/get from postman. So, postman is acting as client and postman-echo/get is acting as API server. After getting the above request, API server processed it and respond back to postman. At last postman received the response and displayed in the response body.
<img width="960" alt="My first request" src="https://user-images.githubusercontent.com/102998720/165429567-779b0687-211d-4ea7-86a8-ffa595c8007e.png">

2. Create your first collection, Collection Name: api-lab
- Save your request from step 1 in collection
- Save all your requests in this collection

Ans. First I have created a new collection by clicking the "+" beside collection tab and named it as api-lab. Then I saved the request "GET postman-echo.com/get" to that collection.
<img width="960" alt="my first collection" src="https://user-images.githubusercontent.com/102998720/165430550-ea2bf21a-b813-41df-9ced-14ac260731e0.png">

3. Building Requests
Document was covered thoroughly.

Make API calls using the following URIs and record the status code and response body for each API call


1. Get authentication token using URI: https://postman-echo.com/basic-auth.
How did you get the response?
Ans. When I tried to send request, the response was showing "unauthorized" with status 401-Unauthorized.
Then I got the response by selecting Authorization as Basic Auth with the following username and password:

username: postman
password: password
<img width="960" alt="Basic-auth" src="https://user-images.githubusercontent.com/102998720/165431232-9609eb80-9f59-419b-a1ba-b206191d9679.png">

2. Get information about all users using URI: https://reqres.in/api/users.
How many lists can you see in the response body?
Ans: I can see one list "data" in the response body.
{
    "page": 1,
    "per_page": 6,
    "total": 12,
    "total_pages": 2,
    "data": [
        {
            "id": 1,
            "email": "george.bluth@reqres.in",
            "first_name": "George",
            "last_name": "Bluth",
            "avatar": "https://reqres.in/img/faces/1-image.jpg"
        },
        {
            "id": 2,
            "email": "janet.weaver@reqres.in",
            "first_name": "Janet",
            "last_name": "Weaver",
            "avatar": "https://reqres.in/img/faces/2-image.jpg"
        },
        {
            "id": 3,
            "email": "emma.wong@reqres.in",
            "first_name": "Emma",
            "last_name": "Wong",
            "avatar": "https://reqres.in/img/faces/3-image.jpg"
        },
        {
            "id": 4,
            "email": "eve.holt@reqres.in",
            "first_name": "Eve",
            "last_name": "Holt",
            "avatar": "https://reqres.in/img/faces/4-image.jpg"
        },
        {
            "id": 5,
            "email": "charles.morris@reqres.in",
            "first_name": "Charles",
            "last_name": "Morris",
            "avatar": "https://reqres.in/img/faces/5-image.jpg"
        },
        {
            "id": 6,
            "email": "tracey.ramos@reqres.in",
            "first_name": "Tracey",
            "last_name": "Ramos",
            "avatar": "https://reqres.in/img/faces/6-image.jpg"
        }
    ],
    "support": {
        "url": "https://reqres.in/#support-heading",
        "text": "To keep ReqRes free, contributions towards server costs are appreciated!"
    }
}

3. Get information about the user with id 3 using URI: https://reqres.in/api/users/3.
How many lists can you see in the response body? What are the available property(Key) names in the response body?
Ans. There is no list in the response body.

The primary object have followings property(key):

data
support
Within the object of data we have followings property(key):

id
email
first_name
last_name
avatar
Within the object of support we have followings property(key):

url
text
<img width="960" alt="No3" src="https://user-images.githubusercontent.com/102998720/165432131-cd728c5b-224b-4e3b-aa20-02a60257c0e9.png">

4. Delete the User with id 9 using URI https://reqres.in/api/users/9
What is the response? How many users are now on the users list? https://reqres.in/api/users? Can you see the deleted user record?
Ans. The postman response is 204- No Content.
<img width="960" alt="user9" src="https://user-images.githubusercontent.com/102998720/165432710-38ff6f6f-f1d9-40f2-9294-81f54a36678a.png">

12 users:
{
    "page": 1,
    "per_page": 6,
    "total": 12,
    "total_pages": 2,
    "data": [
        {
            "id": 1,
            "email": "george.bluth@reqres.in",
            "first_name": "George",
            "last_name": "Bluth",
            "avatar": "https://reqres.in/img/faces/1-image.jpg"
        },
        {
            "id": 2,
            "email": "janet.weaver@reqres.in",
            "first_name": "Janet",
            "last_name": "Weaver",
            "avatar": "https://reqres.in/img/faces/2-image.jpg"
        },
        {
            "id": 3,
            "email": "emma.wong@reqres.in",
            "first_name": "Emma",
            "last_name": "Wong",
            "avatar": "https://reqres.in/img/faces/3-image.jpg"
        },
        {
            "id": 4,
            "email": "eve.holt@reqres.in",
            "first_name": "Eve",
            "last_name": "Holt",
            "avatar": "https://reqres.in/img/faces/4-image.jpg"
        },
        {
            "id": 5,
            "email": "charles.morris@reqres.in",
            "first_name": "Charles",
            "last_name": "Morris",
            "avatar": "https://reqres.in/img/faces/5-image.jpg"
        },
        {
            "id": 6,
            "email": "tracey.ramos@reqres.in",
            "first_name": "Tracey",
            "last_name": "Ramos",
            "avatar": "https://reqres.in/img/faces/6-image.jpg"
        }
    ],
    "support": {
        "url": "https://reqres.in/#support-heading",
        "text": "To keep ReqRes free, contributions towards server costs are appreciated!"
    }
}


5. Get information of the user with id 40 using URI: https://reqres.in/api/users/40
How many lists can you see in the response body? What are the available property(Key) names in the response body?
Ans. No list in the response body. No available property was there.
<img width="960" alt="user40" src="https://user-images.githubusercontent.com/102998720/165434290-9385f952-f7da-44d1-a1c1-1890ca5ed78c.png">

6. Create a new user in a system using URI: https://reqres.in/api/users. name: yourname, job: dreamjob
What is the response code: What are the available property(key) names in the response body? What is the value of response Header Etag?
Ans. The response code is 201 Created.

The primary object have followings property(key):

name
job
id
createdAt
<img width="960" alt="6" src="https://user-images.githubusercontent.com/102998720/165444943-0e49efcb-e28b-40f3-863a-4716e8206ff5.png">

7. Sign in to the system using URI: https://reqres.in/api/login and {"email": "peter@klaven"}
What is the response code?
Ans. The response code is 400 Bad Request.
<img width="960" alt="7" src="https://user-images.githubusercontent.com/102998720/165445395-4457bf58-7e74-46e8-8258-1c6255042e06.png">

8. Sign in to the system using URI: https://reqres.in/api/login and
{
"email": "eve.holt@reqres.in",
"password": "cityslicka"
}
What is the value of response Header Etag? What is the response?
Ans. The value of response header Etag is W/"1d-lGCrvD6B7Qzk11+2C98+nGhhuec"

<img width="960" alt="8b" src="https://user-images.githubusercontent.com/102998720/165445848-9046f55d-5959-4d13-95bc-3240b54a3e7b.png">
