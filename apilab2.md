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
<img width="960" alt="8a" src="https://user-images.githubusercontent.com/102998720/165446019-3aee5495-e4cf-464a-b4d5-2df22c97fa20.png">
<img width="960" alt="8b" src="https://user-images.githubusercontent.com/102998720/165446042-be861061-174d-466e-8d7b-c10590b61c67.png">

9. Get information about all planets using URI: https://swapi.dev/api/planets.
Carefully observe the response body and make a list of all attributes and write their data types.
How many lists can you see in the response body?
Ans. There is one list I can see in the response body. Every object under that array has two lists.
<img width="960" alt="9" src="https://user-images.githubusercontent.com/102998720/165446497-e6f42419-b99e-4816-9959-4c6b0701ab66.png">
The data type of the Attributes are given below:

count: number
next: string
previous: null
results: array
name: string
rotation_period: string
orbital_period: string
diameter: string
climate: string
gravity: string
terrain: string
surface_water: string
population: string
residents: array
films: array
created: string
edited: string
url: string

10. Get information about the third planet using URI: https://swapi.dev/api/planets/3/
How many properties you can see in response body?
Ans. 14 properties can be seen here.
<img width="960" alt="10" src="https://user-images.githubusercontent.com/102998720/165447243-d1797f69-67d5-485d-b775-1b0c0b4869f0.png">

11. Get information about all the starships using URI: https://swapi.dev/api/starships.
Carefully observe the response body and make a list of all attributes and write their data types. How many lists can you see in the response body?
Ans. There is one list I can see in the response body. However, every object under that array has two lists.
<img width="960" alt="11" src="https://user-images.githubusercontent.com/102998720/165447590-0233a312-4b2f-46f4-9c28-2bc63335a168.png">

The data type of the Attributes are given below:

count: number
next: string
previous: null
results: array
name: string
model: string
manufacturer: string
cost_in_credits: string
length: string
max_atmosphering_speed: string
crew: string
passengers: string
cargo-capacity: string
consumables: string
hyperdrive_rating: string
MGLT: string
starship_class: string
pilots: array
films: array
created: string
edited: string
url: string

12. Get information about the ninth starship using URI: https://swapi.dev/api/starships/9/
How many lists can you see in the response body?
Ans. I can see two lists.
<img width="960" alt="12" src="https://user-images.githubusercontent.com/102998720/165448037-ea7c52cd-d56c-4272-ad87-7e66767c06a5.png">

13. Get information about all films using URI: https://swapi.dev/api/films. Carefully observe the response body and make a list of all attributes and write their data types.
How many lists can you see in the response body?
Ans. There is one list I can see in the response body. However, every object under that array has five lists.
<img width="960" alt="13" src="https://user-images.githubusercontent.com/102998720/165448261-5bc0eaf2-f7e5-48fe-8ae0-d5ae68d28bd1.png">

14. Get information about the species using URI: https://swapi.dev/api/species
How many lists can you see in the response body?
Ans. I can see one list in the response body.

15. Get all booking ids using URI: https://restful-booker.herokuapp.com/booking
How many lists can you see in the response body?
Ans. I can see one list in the response body.

16. Get details about booking id 23 using URI: https://restful-booker.herokuapp.com/booking/23
What is the response?
Ans. The response is 200 OK - Standard Response for successful HTTP requests. The response is as follows:
<img width="960" alt="image" src="https://user-images.githubusercontent.com/102998720/165448727-3b5b472e-5815-4219-8f04-7510f2148c32.png">

17. Get details about booking id 23 using URI: https://restful-booker.herokuapp.com/booking/3
What is the response?
Ans. The response is 200 OK - Standard Response for successful HTTP requests. The response is as follows:

<img width="960" alt="17" src="https://user-images.githubusercontent.com/102998720/165449095-9ef068b3-0651-4357-ad69-845c9b1369a4.png">

18. Get information about all planets using URI: https://jsonplaceholder.typicode.com/users
What is the response? How many lists can you see in the response body?
Ans. The response is 200 OK - Standard Response for successful HTTP requests. The response is as follows:
<img width="960" alt="18" src="https://user-images.githubusercontent.com/102998720/165449372-761967d5-03e7-4dbb-b86b-e60c3ad6afc9.png">

19. Get information about all species using URI: https://swapi.dev/api/species. Carefully observe the response body and make a list of all attributes and write their data types.
How many lists can you see in the response body? What is the response?
Ans. There is one list I can see in the response body. However, every object under that array has two lists.
<img width="960" alt="19" src="https://user-images.githubusercontent.com/102998720/165449680-c9ea1f32-382a-4ba3-b6b9-66e8f9881830.png">
The data type of the Attributes are given below:

count: number
next: string
previous: null
results: array
name: String
classification: String
designation: String
average_height: String
skin_colors: String
hair_colors: String
eye_colors: String
average_lifespan: String
homeworld: String
language: String
people: array
films: array
created: String
edited: String
url: String
The response is 200 OK - Standard Response for successful HTTP requests.

20. Write JSON path:
a. To retrieve all direct properties of the studio object:

.studio.movie
.studio.music
b. To find out the music’s song:

.studio.music.song
c. To find the rating of all items in the studio:

.studio.movie[0].rating
.studio.movie[1].rating
.studio.movie[2].rating
.studio.movie[3].rating
d. To retrieve information on all movies

.studio.movie[0]
.studio.movie[1]
.studio.movie[2]
.studio.movie[3]
e. To find out the titles of all movies

.studio.movie[0].title
.studio.movie[1].title
.studio.movie[2].title
.studio.movie[3].title
f. To retrieve the titles of all movies by Jack:

.studio.movie[2].director
g. To retrieve the category of the last movie:

.studio.movie[3].category
i. To retrieve all movies that have the isbn property

.studio.movie[2].isbn
.studio.movie[3].isbn
21. Get information about all employees using URI: http://dummy.restapiexample.com/api/v1/employees
How many lists can you see in the response body?
What is the response?
What are the available property(Key) names in the response body?
Make a list of all attributes and write the data types.
Ans. The response body has one list.

The response is 200 OK - Standard Response for successful HTTP requests.

The primary object have following property(key):

status
data
message
Within the array of data we have following property(key):

id
employee_name
employee_salary
employee_age
profile_image
Followings are the data type of all attributes:

status: string
data: array
message: string
id: number
employee_name: string
employee_salary: number
employee_age: number
profile_image: string
<img width="960" alt="21" src="https://user-images.githubusercontent.com/102998720/165450358-424d3637-e058-47f8-84f0-c2ed2fdf41d2.png">
22. Get a single employee data using URI: http://dummy.restapiexample.com/api/v1/employee/3
How many data you can see in response body? What is the response status?
Ans. I can see one data.

The response status is 200 OK
<img width="960" alt="image" src="https://user-images.githubusercontent.com/102998720/165450557-28bd44c2-e314-4452-b003-a8cca0545e55.png">
23.Create a new employee in a system by using URI: http://dummy.restapiexample.com/api/v1/create Verb: POST Request Body:
{
"name":"your name",
"salary":"123",
"age":"23"
}
What is the response? can you see "id" property in the response? if Yes, note the "id" value.
Ans. Standard response for successful HTTP request. Response is as follows:
<img width="960" alt="23" src="https://user-images.githubusercontent.com/102998720/165451164-37853e4a-e2da-42d5-af0a-72a529dcc5f7.png">
The id value is 7680.

24. Delete an employee record whose employee id in 2 by using URI http://dummy.restapiexample.com/api/v1/delete/2
What is the response?
How many employees are now in the employees list? http://dummy.restapiexample.com/api/v1/employees
Can you see the deleted employee record?
Ans. The response is as follows:
<img width="960" alt="24a" src="https://user-images.githubusercontent.com/102998720/165451625-9742b7be-87f1-470c-8b60-1c6c6f5271a7.png">

25. What is the response? What are the available property(Key) names in the response body?
Ans. The response is as follows:
<img width="960" alt="25" src="https://user-images.githubusercontent.com/102998720/165452662-18a2938e-78ac-4bc3-864c-8b2bb56db091.png">
The available property(key) is "error"

26. Get a user Using URL https://reqres.in/api/unknown/2. What is the response?
Ans: The response is as follows:
<img width="960" alt="image" src="https://user-images.githubusercontent.com/102998720/165452964-f6d44d5e-e8de-4d89-99ef-64566f988985.png">
27. A simple health check endpoint to confirm whether the API is up and running using https://restful-booker.herokuapp.com/ping
What is the response?
Ans: The response is as follows:
<img width="960" alt="27" src="https://user-images.githubusercontent.com/102998720/165453170-06b1a9a9-fc29-4339-8dd8-134b42dca8c6.png">

28. Get information using Delayed Response using URI: https://reqres.in/api/users?delay=3
What is the response? How many seconds delay to respond?
Ans: The response is as follows:
<img width="960" alt="29" src="https://user-images.githubusercontent.com/102998720/165453425-4696a544-835e-49ac-91d7-c3e609152830.png">
3:00 seconds delay to respond.

29. Get information about vehicles using URL https://swapi.dev/api/vehicles/schema/
What type of response it is? What is response status code?
Ans: Type of response: Data Not Found

Status Code: 404
<img width="960" alt="29b" src="https://user-images.githubusercontent.com/102998720/165453742-d1b3d0c9-390c-4e1b-9382-c38ab26dc1c7.png">

30. Get information about starships using URL https://swapi.dev/api/starships/schema/
What type of response it is? Write down the response status code.
What are the available property(Key) names in the response body?
Ans. Type of response: Data Not Found

Status Code: 404

Property(Key) name: "detail"
<img width="960" alt="30" src="https://user-images.githubusercontent.com/102998720/165453959-bee17ba2-78ad-41ad-860c-0bac5f218b81.png">



