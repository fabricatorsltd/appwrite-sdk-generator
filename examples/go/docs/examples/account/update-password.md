package main

import (
    "fmt"
    "os"
    "github.com/appwrite/go-sdk"
)

func main() {
    var client := appwrite.Client{}

    client.SetProject("")

    var service := appwrite.Account{
        client: &client
    }

    var response, error := service.UpdatePassword("password", "password")

    if error != nil {
        panic(error)
    }

    fmt.Println(response)
}