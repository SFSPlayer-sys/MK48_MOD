# MK48_MOD 修改版 / MK48_MOD MODIFIED VERSION

**本项目为 Mk48.io 的修改版**

> This is a modified version (MOD) of Mk48.io, released under the GNU AGPL-3.0 license.
---
本版本对[Mk48.io](https://github.com/SoftbearStudios/mk48)增加了游戏数据导出、自定义服务器等。
请勿使用此客户端连接官方服务器！
---

# Mk48.io Game

[![Build](https://github.com/SoftbearStudios/mk48/actions/workflows/build.yml/badge.svg)](https://github.com/SoftbearStudios/mk48/actions/workflows/build.yml)
<a href='https://discord.gg/YMheuFQWTX'>
  <img src='https://img.shields.io/badge/Mk48.io-%23announcements-blue.svg' alt='Mk48.io Discord' />
</a>

![Logo](/client/logo-712.png)

[Mk48.io](https://mk48.io) is an online multiplayer naval combat game, in which you take command of a ship and sail your way to victory. Watch out for torpedoes!

- [Ship Suggestions](https://github.com/SoftbearStudios/mk48/discussions/132)

## Build Instructions

1. Install `rustup` ([see instructions here](https://rustup.rs/))
2. Install `gmake` and `gcc` if they are not already installed.
3. Install `trunk` (`cargo install --locked trunk --version 0.17.5`)
4. Run `download_makefiles.sh`
5. Install Rust Nightly and the WebAssembly target

```console
make rustup
```

6. Build client

```console
cd client
make release
```

7. Build and run server

```console
cd server
make run_release
```

8. Navigate to `https://localhost:8443/` and play!

## Developing

If you follow the *Building* steps, you have a fully functioning game (could be used to host a private server). If your goal
is to modify the game, you may want to read more :)

### Entity data

Entities (ships, weapons, aircraft, collectibles, obstacles, decoys, etc.) are defined at the bottom of
`common/src/entity/_type.rs`.

### Entity textures

Each entity type must be accompanied by a texture of the same name in the spritesheet, which comes with the
repository. If entity textures need to be changed, see instructions in the `sprite_sheet_packer` directory.

## Contributing
See [Contributing](https://github.com/SoftbearStudios/mk48/wiki/Contributing) Wiki page.

## Trademark

Mk48.io is a trademark of Softbear, Inc.
