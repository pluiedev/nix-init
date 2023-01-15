# nix-init

[![release](https://img.shields.io/github/v/release/nix-community/nix-init?logo=github&style=flat-square)](https://github.com/nix-community/nix-init/releases)
[![version](https://img.shields.io/crates/v/nix-init?logo=rust&style=flat-square)](https://crates.io/crates/nix-init)
[![deps](https://deps.rs/repo/github/nix-community/nix-init/status.svg?style=flat-square&compact=true)](https://deps.rs/repo/github/nix-community/nix-init)
[![license](https://img.shields.io/badge/license-MPL--2.0-blue?style=flat-square)](https://www.mozilla.org/en-US/MPL/2.0)
[![ci](https://img.shields.io/github/actions/workflow/status/nix-community/nix-init/ci.yml?label=ci&logo=github-actions&style=flat-square)](https://github.com/nix-community/nix-init/actions?query=workflow:ci)

Generate Nix packages from URLs (WIP)

- Hash prefetching powered by [nurl]
- Dependency inference for Rust packages using the [Riff](https://github.com/DeterminateSystems/riff) registry
- Interactive prompts with fuzzy tab completions
- License detection
- Supported builders
  - `stdenv.mkDerivation`
  - `rustPlatform.buildRustPackage`
  - `buildGoModule`
- Supported fetchers
  - `fetchCrate`
  - `fetchFromGitHub`
  - `fetchFromGitLab`
  - All other fetchers supported by [nurl](https://github.com/nix-community/nurl) are also supported, you just have to specify the tags manually

## Usage

```
Usage: nix-init [OPTIONS] <OUTPUT>

Arguments:
  <OUTPUT>  The path to output the generated file to

Options:
  -u, --url <URL>  Specify the URL
  -h, --help       Print help
  -V, --version    Print version
```

## Changelog

See [CHANGELOG.md](CHANGELOG.md)

[nurl]: https://github.com/nix-community/nurl