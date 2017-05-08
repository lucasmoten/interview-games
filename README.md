# interview-games

# Go(lang) Coding Demonstration

Supply buildable source code that runs as a simple webserver.

The webserver is for storing clients' favorite foods. It should expose two API
operations:

* `GET` on a route "/foods" to return a list of all your favorite foods
* `POST` on the same route "/foods" to add a food to the list

Add functionality for deleting and accessing foods by ID for extra credit.

Using 3rd party frameworks and libraries is great! Just make sure we can fetch
your code's dependencies with `go get`.

## Technical Requirements

The data model and server implementation are up to you. We have some specific
requirements around configuration and security:

* Protect your API and differentiate your API's clients with some kind of client token scheme
* Valid client tokens should be read from some kind of config file on startup
* If a client tries to call the API with a token that is not in the file, return an error
* Provide an example config with your submission
* Use BoltDB as your API's simple persistance layer

## Deliverable Requirements

We want more than clean code. Include some basic API documentation and
build instructions in your README.

## Getting Started

Here's a **main.go** file to get you started.

```go
package main

import (
	"flag"
	"fmt"
	"github.com/boltdb/bolt"
)

// Config
var (
	port = flag.String("port", "8080", "port for the server to listen on")
)

// DB is our global handle to bolt
var db *bolt.DB

// tokens is the list of valid client tokens
var tokens []string

func main() {
   // parse flags, load config, open db, start server
}

```

## How to Submit

Please provide a link to a public repository, or put all of your assets into
a .zip file.

# Got a Question?

If you need clarification on any of the tasks outlined, feel free to send
us an email at **coleman.mcfarland [at] deciphernow.com**
