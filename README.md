# Cotton Pyramid 👁️‍🗨️ 

This is a custom pipe for https://github.com/mediar-ai/screenpipe which monitors your social messagers activity 👁️👁️👁️

# Getting Started

1. Build screenpipe CLI as described in https://docs.screenpi.pe/docs/getting-started

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- --no-modify-path
brew install pkg-config ffmpeg jq cmake wget
curl -fsSL https://bun.sh/install | bash
git clone https://github.com/mediar-ai/screenpipe
cd screenpipe
cargo build --release --features metal
./target/release/screenpipe # <-- this runs fresh screenpipe
```

2. [OPTIONAL] Build screenpipe FRONTEND as described in https://docs.screenpi.pe/docs/getting-started

```
cd screenpipe-app-tauri
bun install
bun scripts/pre_build.js # <- this is important to copy the CLI into the app
bun tauri build
```

3. Install ollama https://ollama.com/download

4. Download this particular llama3.2 model: `ollama run llama3.2:3b-instruct-q4_K_M` https://ollama.com/library/llama3.2:3b-instruct-q4_K_M

5. Set OPENAI_API_KEY envoronment variable:
```
export OPENAI_API_KEY=...
```

6. Install pipe to screenpipe:

```
git clone git@github.com:sundai-club/pyramid.git
# screenpipe pipe download https://github.com/sundai-club/pyramid/ # <-- not sure why it's not working this way
screenpipe pipe download pyramid
screenpipe pipe enable pyramid
```

7. Run screenpipeL

```
screenpipe
```
