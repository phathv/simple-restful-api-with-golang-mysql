# simple-restful-api-with-golang-mysql
simple restful api CRUD using golang and mysql db

# step to run
 - create db name on mysql phpmyadmin "todo"
   This line will connect mysql db
   err = gorm.Open("mysql", "root:password@/todo?charset=utf8&parseTime=True&loc=Local")
   while root is db username, password is db password
 - run mysql db server
 - Open terminal and run command: go build main.go
 - use postman to check how your api work.
    - create a todo
      - POST http://localhost:8080/api/v1/todos
        {"title":"todo 1", "completed": 1}
    - get all todos
      - GET http://localhost:8080/api/v1/todos
    - update a todo id = 1
      - PUT http://localhost:8080/api/v1/todos/1
    - get a todo id = 1
      - GET http://localhost:8080/api/v1/todos/1
    - delete a todo id = 1
      - DELETE GET http://localhost:8080/api/v1/todos/1
