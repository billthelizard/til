## Logging

```go
package main

import (
	"io"
	"log"
	"os"
)

func LoggingSettings(logFile string) {
	logfile, _ := os.OpenFile(logFile, os.O_RDWR|os.O_CREATE|os.O_APPEND, 0666)
	multiLogFile := io.MultiWriter(os.Stdout, logfile)
	log.SetFlags(log.Ldate | log.Ltime | log.Llongfile)
	log.SetOutput(multiLogFile)
}

func main() {
	LoggingSettings("test.log")
	_, err := os.Open("GOIHIHUIH")
	if err != nil {
		log.Fatalln("Exit", err)
	}
}
```

## Output

```console
2019/06/10 00:09:51 /Users/billthelizard/dev/go/lesson.go:20: Exit open GOIHIHUIH: no such file or directory
```
