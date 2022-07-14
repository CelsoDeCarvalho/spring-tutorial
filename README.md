# spring-tutorial
### Tutorial for using best practices in developing a rest api in spring boot

In this small tutorial we will learn how to create api rest with the spring boot framework and we will discuss the DTO's, 
pagination, filters and sorting of the api in order to achieve the best practices of developing an api rest with springboot.

## DTO
The dto is an object where only the attributes that the end user will need to interact with are considered.

```
public class User{
  private String username;
  private String name;
  private String password;
  private boolean isAdmin;
}

Saving `User` entity `json`

"name":"Celso Momade",
"username":"celso"
"password":"12345",
"isAdmin":"false
```
This would be the json to be sent as the body of the request to the user's post, but it is not correct to leave the isAdmin 
field filled during the save, so the dto will be used to create an object with attributes necessary for the save process.

### UserDto
```
public class UserDto{
  private String username;
  private String name;
  private String password
}

Saving `DtoUser` entity `json`

"name":"Celso Momade",
"username":"celso"
"password":"12345",
```
