## TASKS

### Description
    This plugin allows a user to retrieve a list of available tasks.
    
### Endpoint
    */task*
    
### Http request method
    *GET*
    
### Parameters
    No Parameters
    
### Responses
- Successful operation
  - Status code: 200
- Not Found
  - Status code: 400


## CREATE TASKS

### Description
    This plugin allows a user to create tasks for an organisation.

### Endpoint
    */add-task*
    
### Http request method
    *POST*
    
### Parameters
| Name            | Data type | Description            |
| --------------- | --------- | ---------------------- |
|       _id       | string    | MongoDB define the id  |
|   user_id       | string    | The current user id    |
|   title         | string    | Title of the task      |
|   description   | string    | Task description       |
|   status        | string    |set status(Pending, overdue, complete)|


### Responses
- Success
  - Description: Creates tasks
  - Status code: 200
  - Response body:  
     
 ```sh
    {
       "_id": "string",
       "user_id": "string",
       "title": "doggie",
       "description": "string",
       "status": "pending",
       "start_date": "string",
       "end_date": "string",
       "deleted_date": "string",
       "archive_at": "string",
       "recurring_data": {},
       "labels": "string",
       "collaborators": [
        "string"
       ]
    }
  ```
  
  - Description: Invalid input 
  
  - Status code: 400