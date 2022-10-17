# User authentication using FastAPI (a python frameworks), MongoDB (for database), Docker Compose (for deployment)

**The commands:**

```  
Start the application:
```
$ docker-compose up -d
```
The above command will both create the images and start the containers (2 images and 2 containers - one for the FastAPI application and one for the MongoDB database).

For visualizing the application, open up your browser and enter:

* http://127.0.0.1/docs

In the application we have seven sections:
* For authentication (the right green "Authorize" button from the above);
* For creating users (3 roles are acceptable only: "admin", "dev", "simple mortal", you'll see an error if not respecting the rule);
* For creating tokens by entering user's credentials;
* For listing the users;
* For watching the current user (only if authenticated);
* For modifying user properties (only if authenticated with admin role);
* For deleting the user.

To see the runing containers in docker, enter in the terminal:
```
$ docker ps
```
To see the database and collection created (database name is: myTestDB, collection: users) enter in your terminal:
```
$ docker exec -it <container-id> bash
```