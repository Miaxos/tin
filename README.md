<div align="center">

<img src='docs/logo.svg' width=250px />

<br/>
<h4>Rust GraphQL Template 🏗️</h4>

<a href="https://github.com/azzamsa/tin/actions/workflows/ci.yml">
    <img src="https://github.com/azzamsa/tin/actions/workflows/ci.yml/badge.svg" alt="Build status" />
  </a>

</div>

---

## Features

- [Async-GraphQL](https://github.com/async-graphql/async-graphql) GraphQL server library
  - Relay-compatible cursor-based pagination
  - Playground disabled in the production environment for performance reasons
  - Store GraphQL schema to file automatically
- [SQLx](https://github.com/launchbadge/sqlx) SQL toolkit
- [Axum](https://github.com/tokio-rs/axum) web framework
- [Tracing](https://github.com/tokio-rs/tracing) with local timestamp.
- [utoipa](https://github.com/juhaku/utoipa) Auto-generated OpenAPI documentation
- [git-cliff](https://github.com/orhun/git-cliff) Changelog Generator
- Exhaustive Integration tests
  - Uses [Cynic](https://github.com/obmarg/cynic) for GraphQL client
  - [Hurl](https://github.com/Orange-OpenSource/hurl) for E2E test
- GitHub Action for CI and release
- Git hooks for continuous development (format, lint, test)
  - Uses [Cargo Husky](https://github.com/rhysd/cargo-husky)
- Consistent formatting using [dprint](https://github.com/dprint/dprint)
- [cargo-binstall](https://github.com/cargo-bins/cargo-binstall) support

## Variations

- [Without the database](https://github.com/azzamsa/tin/tree/no-database)

## Checklist

When you use this template, try to follow the checklist to update your info properly

- [ ] Change the author name in `LICENSE`
- [ ] Change the package info in `Cargo.toml`
- [ ] Change the application name:
  - [ ] Database name and other values in `.env` and `.example.env` file.
  - [ ] The OpenAPI info in `routes.rs`
  - [ ] App name in `release.sh`
  - [ ] App name in `release.yml`
  - [ ] App name in the import statements across Rust source and tests files.
- [ ] Clean up the READMEs and remove routes

And, enjoy :)

## Usage

```shell
$ # Clone the repository

$ # Create a database
$ sudo -u postgres createdb tin

$ touch $SCHEMA_LOCATION # See .example.env
$ just dev  # See also `just setup`
```

Go to the playground `http://127.0.0.1:8000/playground` to see the schema.

## Navigating the Code

All the features can be found in the [CHANGELOG](CHANGELOG.md) file tagged with `feat`.
The file only contains user-facing changes, so you won't get lost navigating the code.

## Credits

- [Clean and Scalable Architecture for Web Applications in Rust](https://kerkour.com/rust-web-application-clean-architecture) by Sylvain Kerkour
- Icons and emoji from [Noto Emoji](https://github.com/googlefonts/noto-emoji)
