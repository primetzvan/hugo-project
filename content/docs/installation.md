---
title: "Installation"
date: 2021-10-12T15:13:44+02:00
---

## Manual

### DB

First you have to open the *leo-database-learner-project* in any development environment.
We used the *IntelliJ IDEA Ultimate* environment. Make sure you use Linux or MacOS.

Then open your terminal and make sure that the path is correct:

e.g.

```
/Users/user/Desktop/project_itp/leo-database-learner/leo-database-learner-project
```
After this you have to write the following into your terminal:


#### Linux / MacOS

##### start db
```
cd ./docker
docker-compose up --build -d
```

or you can use a script

```
./run-db.sh
```

##### stop db

```
docker-compose down
```

#### Win

##### run db
```
cd ./docker
docker-compose -f docker-compose-volume.yml up --build -d
```

or you can use a script

```
run-db.bat
```

##### stop db

```
docker-compose down
```

Click on "+" in the database window. Then select the following (as shown in the picture)
and create 2 PostgreSQL databases:

image::startdb01.png[]

*Studentdb*

So make sure that everything looks exactly like this and the password is *app*.
Then test the connection and if everything works it should look like the picture.

image::startdb02.png[]

*Operativedb*

So make sure that everything looks exactly like this and the password is *app*.
Then test the connection and if everything works it should look like the picture.

image::startdb03.png[]


If you have updated the docker-compose and nothing changed try this:

```
docker-compose up --build
docker-compose down
docker volume prune
```

### Backend

Check if you are in the backend folder.

```
~/leo-database-learner/leo-database-learner-project
```

To start the backend project enter following code into the terminal:

```
./mvnw clean compile quarkus:dev
```

### Frontend

Check if you are in the frontend folder.

```
~/leo-database-learner/leo-database-learner-frontend
```

To start the backend project enter following code into the terminal:

```
npm install
```

```
ng serve --open
```




