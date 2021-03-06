<p align="center">
  <a href="url">
    <img src="https://github.com/kioie/gcp-secret-manager/blob/master/.github/Logo.gif" alt="Go GCP Secret Manager" width=400 height=150>
  </a>
  <h2 align="center">Go GCP Secret Manager</h2>

  <p align="center">
    If you are working on GCP Secret Manager, this package is a useful place to start. It offers simple and easy integrations. Use this package to get started.
    <br>
    </p>
</p>

<br>

[![codecov](https://codecov.io/gh/kioie/gcp-secret-manager/branch/master/graph/badge.svg)](https://codecov.io/gh/kioie/gcp-secret-manager)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://github.com/kioie/gcp-secret-manager/blob/master/LICENSE)
[![Actions Status](https://github.com/kioie/gcp-secret-manager/workflows/Go/badge.svg)](https://github.com/kioie/gcp-secret-manager/actions)
[![Go Report Card](https://goreportcard.com/badge/github.com/kioie/gcp-secret-manager)](https://goreportcard.com/report/github.com/kioie/gcp-secret-manager)
[![Open Source Love](https://badges.frapsoft.com/os/v2/open-source.png?v=103)](https://github.com/ellerbrock/open-source-badges/)


A simple golang package for reading, writing, deleting, storing and editing secrets on Google Cloud Secret Manager.

With extensive test coverage and benchmarks.
## Features
  * Lightweight and fast
  * Native Go implementation. 
  * Context based client authorization
  * Integrated API wrapper
  * Improved API error handlers
  * Improved CRUD operations on GCP Secrets

## Installation

Install the package to your [$GOPATH](https://github.com/golang/go/wiki/GOPATH "GOPATH") with the [go tool](https://golang.org/cmd/go/ "go command") from shell:
```bash
$ go get github.com/kioie/gcp-secret-manager
```

## Requirements

`gcp-secret-manager` package tested against `Go >= 1.13.x`.

## Usage
Import the `gcp-secret-manager` package
``` go
import "github.com/kioie/gcp-secret-manager"
```
Declare global variable `ProjectID`
``` go
ProjectID="<your-project-id>"
```
## Example

``` go
package main  
  
import (  
   "fmt"  
   "github.com/kioie/gcp-secret-manager"  
)  
  
func main() {  
 //Declare ProjectID
   ProjectID = "secret-manager-test"  
   //Check if "my-secret" exists
   fmt.Println(gcp_secret_manager.SecretExists("my-secret"))  
   //Get the secret  
   result, _ := gcp_secret_manager.GetSecret("my-secret", "")  
   fmt.Println(result)
}
```
## Contributors

<a href="https://github.com/kioie/gcp-secret-manager/graphs/contributors">
  <img src="https://contributors-img.web.app/image?repo=kioie/gcp-secret-manager" />
</a>

## Copyright

Copyright © 2020 Eddy Kioi

Go GCP-SECRET-MANAGER package released under [Apache License](https://github.com/kioie/gcp-secret-manager/blob/master/LICENSE) .