# Http server
## 1. Create http server by compiling golang binary.
- Download and install the Go distribution
  - [Getting Started](https://golang.org/doc/install)
  - [Code organization](https://golang.org/doc/code.html#Organization)
- Use below code to compile binary.
```
package main

import (
	"flag"
	"fmt"
	"log"
	"net/http"
	"time"
)

var (
	PORT  = flag.Int("port", 80, "Server port")
	DELAY = flag.Int("delay", 150, "delay in millisecond")
	LOGS  = flag.Bool("logs", false, "Show logs")
)

func main() {

	flag.Parse()

	http.HandleFunc("/", handler)

	err := http.ListenAndServe(fmt.Sprintf(":%d", *PORT), nil)

	fmt.Printf("ListenAndServe: %v\n", err)
}

func handler(w http.ResponseWriter, r *http.Request) {

	logs("start")

	time.Sleep(time.Duration(*DELAY) * time.Millisecond)

	logs("end")

	fmt.Fprint(w, "quack")
}

func logs(format string, v ...interface{}) {
	if *LOGS {
		log.Printf(format, v...)
	}
}
```
