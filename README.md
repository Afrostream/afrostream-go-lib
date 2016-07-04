# Description

sets of Afrostream API for golang

# API

## env

```
val := env.Read(key)
val := env.ReadAsUint(key)
val := env.ReadAsUint16(key)
```

## log

```
log.Log(log.ERROR, "printed string: %s", "bouh !")
```

## server

using "echo" engine

```
server := server.New()
server.engine.GET("/hello-world", func(c echo.Context) error {
  return c.String(http.StatusOK, "Hello, World!")
})
server.Spawn("8000")
```
