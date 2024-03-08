**Swivl Company Backend Assignment**

Recipe Sharing Platform with OOP

**Database: Sqlite**

Classes: 

    1.User
  
    2.Recipe


**User Class Methods:**

    1.register : This method is useful to register a new user. If successfully registered, it will send the 'Id' of the user.
    
    2.authorization : This method useful to identify the user , if verified successfully , it will generate a json web token and send to the user, which is used in further request in request headers
    
    3.profileManagement : This method is useful to get the details of a specific user based on user id.
    
    4.updateProfile : This method is useful to update the details of a specific user based on the user id .
    
    5.UserDelete : This method is useful to delete a specific user from the database based on user id.
    

**Recipe Class Methods**

    1.addRecipe : This method is useful to add new Recipe to database , sends the id of new Recipe.

    2.getRecipe : This method is useful to get a specific recipe based on the recipe id.

    3.updateRecipe : This method is useful to update the details of a specific recipe based on the recipe id.

    4.DeleteRecipe : This method is useful to delelte a specific recipe based on the recipe id.


**Database Files**:

    1.user.db : Contains **user** table

    2.recipe.db : Contains **recipe** table


**Backend Project Live Link** : **https://swivlbackendassignment.onrender.com**


**API**

**USER CLASS API'S**

**1.Registration**

    Path: /register
    
    Method : POST

    Description : This method is useful to register a new user. If successfully registered, it will send the 'Id' of the user.
    
    Sample API : https://swivlbackendassignment.onrender.com/register
    
    Request Body :
    
        {
        "username": "aeatockj",
        "password": "szWAG6hc",
        "email": "aeatockj@psu.edu",
        "image": "https://robohash.org/Lenna.png?set=set4"
        }

    Response:
    
        Registration Successful ,id=21

**2.Login**

    Path: /auth

    Method : POST

    Description : This method useful to identify the user , if verified successfully , it will generate a json web token and send to the user, which is used in further request in request headers

    Sample API : https://swivlbackendassignment.onrender.com/auth

    Request Body :

        {
            "username": "aeatockj",
            "password": "szWAG6hc"
    
        }

    Response :

        {
            "jwtToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MjEsInVzZXJuYW1lIjoiYWVhdG9ja2oiLCJpYXQiOjE3MDk4ODAyNDd9.q3UsGBfwyFD950tXKhos7T2a762wyDn8gY7XDytm-pM"
        }

**3.Profile Management**

    Path : /userProfile/:id

    Method : GET 

    Description : This method is useful to get the details of a specific user based on user id.

    Sample API : https://swivlbackendassignment.onrender.com/userProfile/3

    Response : 

        {
            "id": 3,
            "username": "swivl company",
            "password": "1234#123",
            "email": "swivl@`123",
            "image": "https://source.unsplash.com/user/c_v_r/1900x800"
        }

**4.Update User Profile**

    Path : /updateProfile/:id

    Method : PUT

    Description :  This method is useful to update the details of a specific user based on the user id 

    Sample API : https://swivlbackendassignment.onrender.com/updateProfile/3

    Request Body: 

        {
            "username": "Jocky",
            "password": "szWAG6hc",
            "email": "Jack@123",
            "image": "https://source.unsplash.com/user/c_v_r/1900x800"
    
        }

    Response: 

        User profile updated Successfully

**5 Delete Profile**

    Path : /deleteUser/:id

    Method : DELETE

    Description : This method is useful to delete a specific user from the database based on user id

    Sample API : https://swivlbackendassignment.onrender.com/deleteUser/20

    Response : 

        User Deleted Successfully
