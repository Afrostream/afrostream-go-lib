# Description

sets of Afrostream API for golang

# Install

## Install golang

you need golang 1.6
you need to set your *$GOPATH* env var (assuming ~/go here.)

## Install this library

```
cd $GOPATH/src
mkdir -p $GOPATH/src/github.com/afrostream
cd $GOPATH/src/github.com/afrostream
git clone git@github.com:Afrostream/afrostream-go-lib.git
```

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
