---
pageId: "251265219"
spaceId: "250642439"
confluenceUrl: https://everypeer.atlassian.net/wiki/spaces/TS/pages/251265219/Word_Counter

---
---

Description: Takes a string as an input and then uses a map to count each instance of a word to give a total tally

---

```go
package main

import (
	"bufio"
	"fmt"
	"os"
	"strings"
)

func main() {
	
	reader := bufio.NewReader(os.Stdin)
	
	fmt.Print("Enter a string: ")
	str, err := reader.ReadString('\n')
	if err != nil {
		fmt.Println("Error reading input: ", err)
	os.Exit(1)
	}
	
	sentence := strings.Fields(str)
	
	words := make(map[string]int)
	
	for i := 0; i <= len(sentence) - 1; i++ {
		words[sentence[i]]++
	}
	
	fmt.Println("\nWord Count:")
	for word, count := range words {
		fmt.Printf("%s: %d\n", word, count)
	}
	
	os.Exit(0)
}
```

---
