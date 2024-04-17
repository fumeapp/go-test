# Fiber+Fume example
> Example setup of a Fiber project running in Fume

<p align="center">
  <img src="https://github.com/fumeapp/fiber-example/blob/production/fiber-example.png?raw=true" />
</p>

```go
package main

import (
	fume "github.com/fumeapp/fiber"
	"github.com/gofiber/fiber/v2"
)

func main() {
	app := fiber.New()
	app.Get("/", func(c *fiber.Ctx) error {
		return c.Status(200).JSON(&fiber.Map{"message": "Fiber running with Fume"})
	})
	fume.Start(app, fume.Options{})
}
```
deployment 3 test
