# Fish World
A fun game where the user can help clean the ocean.
A mix of fish and garbage will come out from the ocean and the
user will be able to click on the garbage giving them points for 
each garbage they distroy but if they click on a fish the game is over.

We did this using Golang!!

## Install Golang !!
* https://golang.org/doc/install

###Installing Packages: 
* https://golang.org/pkg/
* http://www.alexedwards.net/blog/serving-static-sites-with-go
* Declare package at the top of every source file

###Packages
* Execut­ables should be in package main
* Upper case identifier: exported (makes it visible from other packages)
* Lower case identifier: private (not visible to other packages)


##Why Golang?
Golang is a good fit for anyone due to its simplicity, speed, and high performance. It is also
usable across multiple platforms, has multiple built-in language features. As well as an 
efficient garbage collector. It is used by many big companies such as Google, Dropbox, and 
Soundcloud. Golang has the speed of a compiled laguage but the feel of 
an interpreted language, making writting code fast and allowing for rapid feedback.
There are not classes or inheritance in Go but they do have 
structs which can have methods to them. You can use arrays, if statements, loops, and switch.
In order for golang to work you need packages and imports. You could use 
multiple imports.

```
package main 
import (
    "net/http"
    "log"
    "fmt"
)
func main () {
  fmt.Printf("Hello World")
}
```

## Golang syntax examples
### Variables
####Declaring a variable
```
var varname vartype

```
####Declaring a variable with a value

```
var varname vartype = value
```
### Functions
####Simple functions

```
func functionName() {
    
}
```
####Functions with Parameters
```
func functionName(param1 string, param2 int) {
    
}
```

## Built-in  Types
* bool (boolean)
* string
* int (8, 16, 32, 64)
* float (32, 64)

## Team Jared Members
[Dominique Alexander](https://github.com/domo1664)
[Miriam Hernandez](https://github.com/miriamhz14)
[Michael Rivera](https://github.com/Itseasymike)
[Marcos Wade](https://github.com/Paraone)

This is an example of an api call using Golang
```
package main

import (
    "fmt"
    "net/http"
    "io/ioutil"
)

func main() {

//api url
url := "https://www.googleapis.com/youtube/v3/search?part=snippet&key=APIKEY_HERE"

//sending get request
req, _ := http.NewRequest("GET", url, nil)

//getting the response
res, _ := http.DefaultClient.Do(req)

//closing the response body
defer res.Body.Close()
body, _ := ioutil.ReadAll(res.Body) //reading the response

fmt.Println(res)
fmt.Println(string(body))

}
```
