# GolangMgoRestServer


0. pkg 를 가져와 봅니다.
//echo
//Fast and unfancy HTTP server framework for Go (Golang). Up to 10x faster than the rest.
go get -u github.com/labstack/echo

//mongodb driver golang
//Firebase 에도 사용되고 있지요?
go get gopkg.in/mgo.v2


1. local mongodb 를 실행 후 golang server 를 실행해 봅니다.
go run main.go
//이런 결과가 나오겠지요.
=>  Running at :3333


2. 주소는 아래와 같습니다.
http://localhost:3333

body message 는 아래와 같습니다.
{
  "TodoMessage": "foo bar"
}


3. http://localhost:3333/api/todos/ 입니다.
func Init(e *echo.Echo) {
	e.GET("/api/todos", todocontroller.GetAll)
	e.GET("/api/todos/:id", todocontroller.GetById)
	e.POST("/api/todos", todocontroller.NewTodo)
	e.DELETE("/api/todos/:id", todocontroller.RemoveTodo)
}


