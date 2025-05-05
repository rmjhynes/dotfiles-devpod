# DevPod Dotfiles 🐋
_**Dev-Environment-as-Code**_

A repo to setup a Dev Container with the packages that I typically use. This could potentially be used as a template for other dev containers if I needed to create one on a per project basis.

## DevPod
[Dev containers](https://containers.dev/) were designed to work with VSCode. Since I don't use VSCode on my personal machines and prefer to use Neovim, I needed a solution to run them without being locked into a vendor / IDE.

[DevPod](https://devpod.sh/) is an open source equivalent that you can use with any IDE and makes it very easy to SSH into the container so that you can use a terminal-based editor such as Neovim.

## Package Management
Dev containers have many [Features](https://containers.dev/features) available that you can use in place of packages. For now I have stuck to using only the officially maintained Features.

For the rest of the packages that I need, I have installed them with the [Nix Package Manager Feature](https://github.com/devcontainers/features/tree/main/src/nix). Since I am used to using NixOS, I have just copied the packages over from my [nixos-config repo](https://github.com/rmjhynes/nixos-config/blob/main/users/rmjhynes/config/packages.nix).

## VSCode Configuration
Since I do still use VSCode for larger projects, I have configured the settings and declared the extensions that I like in the `.devcontainer/devcontainer.json` spec.
