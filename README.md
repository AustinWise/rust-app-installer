# rust-app-installer

Currently the https://rustup.rs/ website makes it really easy to install a Rust
toolchain. My aspirational goal for this project is:

> Like `rustup`, but for any Rust app.

To reference another existing project:

> Like [trust](https://github.com/japaric/trust), but more accessible to people who are not rust developers.

Without referencing existing projects, I hope to acomplish this with this project:

* Some sample GitHub Actions workflows that make it easy to a Rust project for many platforms.
* Some one-liner shell (and PowerShell) scripts that make it easy for people to acquire pre-built Rust binaries.

## Implementation Details

There are some pieces out there that could be used to create this vision:

* The user-experience of the [trust](https://github.com/japaric/trust) program
* The `TARGET`-detection of [`rustup-init.sh`](https://github.com/rust-lang/rustup/blob/5225e87a5d974ab5f1626bcb2a7b43f76ab883f0/rustup-init.sh)
* The `PATH` management of `rustup`.

One element that does not currently exist in the inspirational codebase is a an
easily copy-pasteable command to install something.

See some work-in-progress in Smeagol:

https://github.com/AustinWise/smeagol/commit/93452a9974fc422a1587789a508db531069158a6

## Why this is a dumb thing to implement

There are a couple reasons why spending effort on this might not be the best use
of my time:

* Making it easier for Rust programs to take advantage of operating systems'
  native distribution methods might be a better use of ones time. See
  [cargo-deb](https://github.com/kornelski/cargo-deb).
