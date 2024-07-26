## How to contribute

1. Fork the repo
2. Make the changes in your fork
3. If you add new `.rs` files in `examples` member add `#![cfg_attr(not(debug_assertions), deny(warnings))]` as first
   line.
4. If you add new members to the workspace add `#![cfg_attr(not(debug_assertions), deny(warnings))]` to it's `lib.rs`
   and to any `bin` files (
   like `main.rs` or other files declared as `[[bin]]`).
5. Add tests for your changes, if applicable
6. `cargo fmt --all`, you can configure your IDE to do this on
   save, [RustRover](https://www.jetbrains.com/help/rust/rustfmt.html)
   and [VSCode](https://code.visualstudio.com/docs/languages/rust#_formatting)
6. `./check-before-push.sh` or `cmd /c check-before-push.bat` and fix any errors
7. Create a PR back to main repo
8. Monitor the checks (GitHub actions run)
9. Respond to any comments
10. In the end, ideally, it will be merged to `main`