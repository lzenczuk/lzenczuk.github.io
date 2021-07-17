### Base REST controller in Rust and Actix-web
Example of typical REST service endpoints implemented in rust.


# Hello world
This is test of gh pages using markdown.

Example of Rust code
```rust
mod products {
    use actix_web::{web, get, Responder, HttpResponse};

    #[get("/products")]
    async fn get_all() -> impl Responder {
        HttpResponse::Ok().body("Hello world!")
    }

    #[get("/products/{product_id}")]
    async fn get_product_by_id(web::Path(product_id):web::Path<u32>) -> impl Responder {
        HttpResponse::Ok().body(format!("Product({})", product_id))
    }

}
```
