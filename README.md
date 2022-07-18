# actix-web-httpauth-proxy

> Proxy version of [actix-web-httpauth](https://github.com/actix/actix-extras/tree/master/actix-web-httpauth).

## About

You send:

* `Proxy-Authorization` header field instead of `Authorization`

The library may return:

* `407 Proxy Authentication Required` header field instead of `401 Unauthorized`

Usage
-----

```toml
actix-web-httpauth-proxy = { git = "https://github.com/ryochin/actix-web-httpauth-proxy", branch = "main" }
```

```rust
use actix_web_httpauth_proxy::extractors::basic::BasicAuth as ProxyAuth;
use actix_web_httpauth_proxy::headers::www_authenticate::{basic::Basic, WwwAuthenticate};
use actix_web_httpauth_proxy::middleware::HttpAuthentication as HttpProxyAuthentication;
```

