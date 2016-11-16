# httpstat

This is a fork of [Dave Cheney's httpstat, itself a Golang version of [reorx's httpstat](https://github.com/reorx/httpstat).
As he has closed the original, which I've found useful (and somewhat superior to the original), this is just a personal copy so I'll always have access in the future.

![Shameless](./screenshot.png)

## Installation
`httpstat` requires Go 1.7.1 or later.
```
$ go get -u github.com/davidprichard/httpstat
```	
## Usage
```
$ httpstat https://example.com/
```
## Features

- HTTP and HTTPS are supported, for self signed certificates use `-k`.
- Skip timing the body of a response with `-I`.
- Follow 30x redirects with `-L`.
- Change HTTP method with `-X METHOD`.
- Provide a `PUT` or `POST` request body with `-d string`. To supply the `PUT` or `POST` body as a file, use `-d @filename`.
- Add extra request headers with `-H 'Name: value'`.
- The response body is usually discarded, you can use `-o filename` to save it to a file, or `-O` to save it to the file name suggested by the server.
- HTTP/HTTPS proxies supported via the usual `HTTP_PROXY`/`HTTPS_PROXY` env vars (as well as lower case variants).
- Supply your own client side certificate with `-E cert.pem`.
