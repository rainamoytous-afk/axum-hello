# Rust + Axum Hello World

## 运行

安装 Rust 后，在项目目录运行：

```sh
cargo run --locked
```

服务启动后，在运行此服务的同一台电脑打开：

http://127.0.0.1:3000/

返回纯文本 `Hello, World!`。

```sh
curl -i http://127.0.0.1:3000/
```

服务监听 `0.0.0.0:3000`。可用 `PORT` 环境变量更改端口，例如：

```sh
PORT=8080 cargo run --locked
```

`127.0.0.1` 是本机地址，不是公网地址。若要让其他电脑通过 HTTP 访问，需要把服务部署到可访问的服务器，并配置相应的端口映射、防火墙或反向代理。

## 测试

```sh
cargo test --locked
```

覆盖首页响应体、Content-Type、404 和 405。
