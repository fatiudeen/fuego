# Echo

Fuego can be seamlessly integrated with the Echo framework using the `fuegoecho` adapter.

Instead of utilizing the default **Server** with `fuego.NewServer()`, you will use the **Engine** with `fuego.NewEngine()`, alongside your Echo router.

The integration process mirrors the default server setup, with the key difference being that you will declare routes using `fuegoecho.Get`, `fuegoecho.Post`, etc., rather than `fuego.Get`, `fuego.Post`.

## Incremental Migration

Follow these steps to gradually integrate Fuego into your Echo application:

1. Instantiate the engine using `fuego.NewEngine()`.
2. Replace `echo.GET` with `fuegoecho.GetEcho` to wrap your routes with OpenAPI declarations, without modifying your existing controllers.
3. Incrementally replace your existing controllers with Fuego controllers, enabling automatic generation of OpenAPI documentation, validation, and content-negotiation for each controller you replace.
4. Enjoy the enhanced functionality provided by Fuego while maintaining compatibility with your existing Echo application.

## Example

For a comprehensive, up-to-date example, please refer to the [Echo example](https://github.com/go-fuego/fuego/tree/main/examples/echo-compat).