# Late Rust SDK

Official Rust client library for the [Late API](https://docs.getlate.dev) - Schedule and manage social media posts across multiple platforms.

## Installation

Add to your `Cargo.toml`:

```toml
[dependencies]
late = "0.1"
```

## Quick Start

```rust
use late::apis::configuration::Configuration;
use late::apis::accounts_api;
use late::apis::posts_api;

#[tokio::main]
async fn main() -> Result<(), Box<dyn std::error::Error>> {
    let mut config = Configuration::new();
    config.api_key = Some(late::apis::configuration::ApiKey {
        key: "YOUR_API_KEY".to_string(),
        prefix: Some("Bearer".to_string()),
    });

    // List accounts
    let accounts = accounts_api::list_accounts(&config).await?;
    println!("{:?}", accounts);

    // Create a post
    let post = posts_api::create_post(
        &config,
        late::models::CreatePostRequest {
            content: Some("Hello from Rust!".to_string()),
            publish_now: Some(true),
            ..Default::default()
        },
    )
    .await?;

    Ok(())
}
```

## Documentation

- [API Reference](https://docs.getlate.dev/api-reference)
- [Getting Started Guide](https://docs.getlate.dev/quickstart)

## License

MIT
