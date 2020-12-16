
To run the demo as a WASM example, a few steps are needed:

cargo install wasm-bindgen-cli
cargo build --target=wasm32-unknown-unknown --example demo
wasm-bindgen ./target/wasm32-unknown-unknown/debug/examples/demo.wasm --out-dir examples/generated --target web

cd examples/
python3 -m http.server

Then browser to http://localhost:8000/ with a WebGL enabled browser.
