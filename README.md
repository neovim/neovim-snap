<h1 align="center">
  <img src="https://raw.githubusercontent.com/neovim/neovim.github.io/master/logos/neovim-logo-300x87.png" alt="nvim">
  <br />
</h1>

<p align="center"><b>This is the snap for nvim</b>. It works on Ubuntu, Fedora, Debian, and other major Linux
distributions.</p>

## Install

### Stable release 

```sh
sudo snap install nvim --classic
```

### Nightly release 
```sh
sudo snap install nvim --edge --classic
```

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/nvim)

## How this repo works

1. This repo defines time-triggered CI jobs which poke its [master](./.github/workflows/update-readme.yaml) and [nightly](./.github/workflows/update-readme-nightly.yaml) branches.
2. The workflow pushes a [timestamp commit](https://github.com/neovim/neovim-snap/commit/752cca5b7c2d8371f54825c61d0c8ebfedbf6711)
   to "tickle" the external Snapcraft service.
3. Snapcraft fetches the `master` or `nightly` branch of this repo and processes `snap/snapcraft.yaml`.
4. Snapcraft builds Nvim (in its own, external service) as defined in `snap/snapcraft.yaml`.
    - The `snap/snapcraft.yaml` in the `nightly` branch is [slightly different](https://github.com/neovim/neovim-snap/compare/master...nightly)
      from the `master` branch. This is a limitation/requirement of Snapcraft's
      design.

## Last Launchpad Sync

<!-- BEGIN SYNC INFO -->
Last sync to launchpad: Wed May 14 11:45:35 UTC 2025
<!-- END SYNC INFO -->
