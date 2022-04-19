<div align="center"><em>Mach is still early stages - see <a href="https://machengine.org/#early-stages">what we have today</a> and <a href="https://twitter.com/machengine">stay tuned</a></em></div>

# Mach: game engine & graphics toolkit for the future

Mach is a game engine & graphics toolkit written in [Zig](https://ziglang.org/) for the future:

* Data-driven, tooling oriented
* Composable
* Competitive with Unity and Unreal in spirit (a fully fledged editor, etc.)

<a href="https://user-images.githubusercontent.com/3173176/163936001-fd9eb918-7c29-4dcc-bfcb-5586f2ea1f9a.gif"><img align="left" src="https://user-images.githubusercontent.com/3173176/163936001-fd9eb918-7c29-4dcc-bfcb-5586f2ea1f9a.gif" alt="boids demo" width="300px"></img></a>

## Cross-platform graphics in ~60 seconds

```sh
git clone https://github.com/hexops/mach
cd mach/
zig build run-example-boids
```

Cross-platform graphics, a unified shader language & compute shaders.

(Requires [zig 0.10.x](https://ziglang.org/) | [known issues](https://github.com/hexops/mach/blob/main/doc/known-issues.md#known-issues))

<img align="right" src="https://machengine.org/img/coder.svg" width="300px"></img>

## Join the conversation

Join us [on Matrix chat](https://matrix.to/#/#hexops:matrix.org) in building the future of game engines & graphics in Zig!

Follow [@machengine on Twitter](https://twitter.com/machengine) for updates.

Contributors are very welcome! There are lots of places you can help out with little knowledge, so feel free to reach out!

## Learn more: [machengine.org](https://machengine.org)

[![](https://user-images.githubusercontent.com/3173176/163927590-6a28d30c-6955-4e9f-9a65-88095aa67299.png)](https://machengine.org)

## Supported platforms

Mach is still early stages, so far we have support for building from the following OS to the following targets:

| Building for     | From macOS x86_64 | From macOS M1/aarch64 | From Linux x86_64 | From Windows x86_64 |
|------------------|-------------------|-----------------------|-------------------|---------------------|
| macOS x86_64     | ✅                | ✅                     | ✅                | ✅                  |
| macOS M1/aarch64 | ✅                | ✅                     | ✅                | ✅                  |
| Linux x86_64     | ✅                | ✅                     | ✅                | ✅                  |
| Windows x86_64   | ✅                | ✅                     | ✅                | ✅                  |
| iOS              | 🏃                | 🏃                     | 🏃                | 🏃                  |
| Android          | 🏃                | 🏃                     | 🏃                | 🏃                  |

* ✅ Tested and verified via CI.
* ✔️ Should work, not tested via CI yet.
* 🏃 Planned or in progress.
* ⚠️ Implemented, but has known issues (e.g. bugs in Zig.)

## Libraries

Mach has many libraries you can use for game development in Zig - you don't have to use the entire engine. All our libraries aim to have the same zero-fuss installation, cross compilation, and platform support:

* [mach-glfw](https://github.com/hexops/mach-glfw): Ziggified GLFW bindings with 100% API coverage
* [mach-gpu-dawn](https://github.com/hexops/mach-gpu-dawn): Google's Dawn WebGPU implementation, cross-compiled with Zig into a single static library 
* [mach-system-sdk](https://github.com/hexops/mach-system-sdk): More libraries for cross-compilation with Zig

## Contributing

Mach is maintained as a monorepo. When changed are merged to this repository, we use some git-fu to pick out the commits to subdirectories and push them ot sub-repositories all automagically. Changes to the `glfw/` directory in this repository get pushed to the separate [mach-glfw](https://github.com/hexops/mach-glfw) repository automagically after being merged here, for example.

Please prefix commits / pull requests with the project name (`glfw: fix an issue`, `gpu: fix an issue`, `examples: fix an issue`, etc.) and if possible only one project per commit. If you don't know how to do this, no worries, we can help!
