## Error Handling

```go
package main

import (
	"fmt"
	"log"
	"os"
)

func main() {
	file, err := os.Open("./lesson.go")
	if err != nil {
		log.Fatalln("Error: file open")
	}
	defer file.Close()
	data := make([]byte, 100)
	count, err := file.Read(data)
	if err != nil {
		log.Fatalln("Error: file read")
	}
	fmt.Println(count, string(data))

	if err = os.Chdir("test"); err != nil {
		log.Fatalln("Error: change directory")
	}
}
```

## Output

```console
100 package main

import (
	"fmt"
	"log"
	"os"
)

func main() {
	file, err := os.Open("./lesson.go")
	if
2019/06/10 00:57:50 Error: change directory
```
