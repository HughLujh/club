# Blog - V1.0

## 1. Introduction

A brief description of the project's purpose and background.

## 2. User-Related Interface

### 2.1 User Sign-up

#### 2.1.1 Basic Description

- Request Path: `/auth/sign-up`
- Request Method: `POST`
- Interface Description: This interface is used for user sign-up

#### 2.1.2 **Request Parameters** Description:

- Request Parameter Format: `application/json`

- Request Parameter Description:

| Parameter Name | Description                            | Type   | Required | Remark                                                       |
| :------------- | :------------------------------------- | ------ | -------- | ------------------------------------------------------------ |
| email          | Email must be unique   in the database | String | Yes      | must meet email format                                       |
| username       |                                        | String | Yes      | This field should not be empty.                              |
| password       |                                        | String | Yes      | Password should have a minimal 8 alphanumeric characters and at least 1 upper letter. |

- Sample Request Data:

```json
{
  "email": "example@example.com",
  "username": "example@example.com",
	"password": "!Mike123123"
}
```

#### 2.1.3 Response Data

- Response Format: `application/json`

- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json
{
    "message": "successfully registered as a personal account",
}
```

```json
{
    "message": "invalid request",
    "errors": {
        "password": "Password should have a minimal 8 alphanumeric characters and at least 1 upper letter.",
        "username": "This field should not be empty."
    }
}
```



### 2.2 User Sign-in

#### 2.2.1 Basic Description

- Request Path: `/auth/sign-in`
- Request Method: `POST`
- Interface Description: This interface is used for user sign-in

#### 2.2.2 Request Parameters Description

- Request Parameter Format: `application/json`

- Request Parameter Details:

| Parameter Name | Description | Type   | Required | Remark                                                       |
| :------------- | :---------- | ------ | -------- | ------------------------------------------------------------ |
| email          |             | String | Yes      | Email must meet email format                                 |
| password       |             | String | Yes      | Password should have a minimal 8 alphanumeric characters and at least 1 upper letter. |

- Sample Request Data:


```json
{
    "email": "example@example.com",
  	"password": !Mike123123
}
```

#### 2.2.3 Response Data

- Response Format: `application/json`

- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json
{
    "message": "successfully signed in",
    "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjMxMjNAZ21haWwuY29tIiwiZW1haWwiOiIxMjMxMjNAZ21haWwuY29tIiwiZXhwIjoxNzI4NjM4MDc3fQ.HinNAMnpla2M_uW-dZ0YPdyPgQ5BaRWO4gIaCy2BOkU"
}
```

```json
{
    "message": "Invalid email or password",
    "errors": {
        "password": "wrong password"
    }
}
```

### 2.3 User Sign out

#### 2.3.1 Basic Description

- Request Path: `/auth/sign-out`
- Request Method: `POST`
- Interface Description: This interface is used for user to sign out

#### 2.3.2 Request Parameters Description

- Request Parameter Format: `application/json`

- Request Parameter Details:

| Parameter Name | Description                     | Type   | Required | Remark                                               |
| :------------- | :------------------------------ | ------ | -------- | ---------------------------------------------------- |
| refreshToken   | The refresh token to be revoked | String | No       | Required if using refresh tokens                     |
| allDevices     | Sign out from all devices       | Bool   | No       | Optional flag to invalidate all tokens(if supported) |

- Sample Request Data:

```json
{
    "email": "example@example.com",
  	"password": !Mike123123
}
```

#### 2.3.3 Response Data

- Response Format: `application/json`

- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json

```



### 2.3 TODO - Retrieve User Basic Information

#### 2.3.1 Basic Description

- Request Path: `/user/profile`
- Request Method: `GET`
- Interface Description: This interface is used for user to retrieve user basic information

#### 2.3.2 Request Parameters Description

- Request Parameter Format: `application/json`

- Request Parameter Details:

| Parameter Name | Description | Type | Required | Remark |
| :------------- | :---------- | ---- | -------- | ------ |
|                |             |      |          |        |
|                |             |      |          |        |

- Sample Request Data:

```json

```

#### 2.3.3 Response Data

- Response Format: `application/json`

- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json

```



### 2.4 TODO - Update User Basic Information

#### 2.4.1 Basic Information

- Request Path: `/user/update`
- Request Method: `PUT`
- Interface Description: This interface is used for the user to update user basic information

#### 2.4.2 Request Parameters Description:

- Request Parameter Format: `application/json`

- Request Parameter Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| username       |             | String | No       |        |
| imageUrl       |             | String | No       |        |

- Sample Request Data:

```json

```

#### 2.4.3 Response Data

- Response Format: `application/json`

- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json

```



### 2.5 TODO - Update User Password

#### 2.5.1 Basic Information

- Request Path: `/user/updatepwd`
- Request Method: `Patch`
- Interface Description: This interface is used for the user to update the password

#### 2.5.2 Request Parameters Description:

- Request Parameter Format: `application/json`

- Request Parameter Details:

| Parameter Name | Description | Type | Required | Remark |
| -------------- | ----------- | ---- | -------- | ------ |
|                |             |      |          |        |
|                |             |      |          |        |
|                |             |      |          |        |

- Sample Request Data:

```json
```

#### 2.5.3 Response Data:

- Response Format: `application/json`

- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json

```



## 3. Post-Related Interface

### 3.1 TODO - Create a new post category

#### 3.1.1 Basic Information

- Request Path: `/category`
- Request Method: `POST`
- Interface Description: This interface is used for the user to create a new post category

#### 3.1.2 Request Parameters Description:

- Request Parameter Format: `application/json`
- Request Parameter Details:

| Parameter Name | Description         | Type   | Required | Remark |
| -------------- | ------------------- | ------ | -------- | ------ |
| categoryName   | category name       | String | Yes      |        |
| categoryAlias  | category alias name | String | Yes      |        |

- Sample Request Data:

```json
{
  "categoryName": "Java",
  "categoryAlias" "SpringBoot"
}
```

#### 3.1.3 Response Data:

- Response Format: `application/json`
- Response Details:

| Parameter Name | Description | Type   | Required | Remark |
| :------------- | :---------- | ------ | -------- | ------ |
| message        |             | String | Yes      |        |
| errors         |             | List   | No       |        |

- Sample Response Data:

```json
```
