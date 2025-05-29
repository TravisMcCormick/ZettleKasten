
```go
package main

import (
"fmt"
"io"
"os"
"strings"
"unicode"
)
  
func main() {

	//Grab arguments
	arg := os.Args[1] 
	
	//Open file
	file, err := os.Open(arg)
	
	if err != nil{
		fmt.Println("Error opening file:", err)
		os.Exit(1)
	}  
	
	//Close file when main ends
	defer file.Close()
	//place after error checking to make sure that the files exists before you try closing something that doesn't exist
	
	//Grab all the content
	content, err := io.ReadAll(file)
	
	if err != nil {
		fmt.Println("Error opening file:", err)
		os.Exit(1)
	}
	
	//Clean content
	cleaned := cleanContent(string(content)) 
	
	//seperate into fields
	sentence := strings.Fields(cleaned)
	
	//Make map for counting
	words := make(map[string]int)
	
	for i := 0; i <= len(sentence) - 1; i++ {
		words[sentence[i]]++
	}
	
	//Print out map
	fmt.Println("\nWord Count:")
	for word, count := range words {
		fmt.Printf("%s: %d\n", word, count)
	}
	os.Exit(0)
}

func cleanContent(input string) string{
	var builder strings.Builder
	
	for _,r := range input {
		if unicode.IsLetter(r){
			builder.WriteRune(r)
		} else if unicode.IsSpace(r){
			builder.WriteRune(' ')
		}
	}
	return builder.String()
}
```