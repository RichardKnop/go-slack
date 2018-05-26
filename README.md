[![Travis Status for RichardKnop/go-slack](https://travis-ci.org/RichardKnop/go-slack.svg?branch=master)](https://travis-ci.org/RichardKnop/go-slack)

# go-slack

A simple Golang SDK for Slack.

## Usage

```go
package main

import (
	"log"

	"github.com/AreaHQ/go-slack"
)

func main() {
	cnf := &slack.Config{IncomingWebhook: "incoming_webhook"}
	adapter := slack.NewAdapter(cnf)
	err = adapter.SendMessage(
		"#some-channel",
		"some-username",
		"message to send",
		"", // emmoji
	)
}
```
