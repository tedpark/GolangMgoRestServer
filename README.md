# GolangMgoRestServer


####0. go get pkg
```
echo is Fast and unfancy HTTP server framework for Go (Golang). Up to 10x faster than the rest.
go get -u github.com/labstack/echo

mgo is mongodb driver golang
ex) Firebase 
go get gopkg.in/mgo.v2
```


####1. run local mongodb and run golang server
```
go run main.go
//You can see this message.
=>  Running at :3333
```

####2. rest api
```
http://localhost:3333/api/todos/

ex) POST body 
{
  "TodoMessage": "foo bar"
}
```

####3. http://localhost:3333/api/todos/
```
func Init(e *echo.Echo) {
	e.GET("/api/todos", todocontroller.GetAll)
	e.GET("/api/todos/:id", todocontroller.GetById)
	e.POST("/api/todos", todocontroller.NewTodo)
	e.DELETE("/api/todos/:id", todocontroller.RemoveTodo)
}
```
