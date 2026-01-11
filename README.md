# Devcontainer Config
_**Dev-Environment-as-Code**_

A repo to setup a Dev Container with the tools that I typically use. This allows me to have a conistsent dev environment regardless of which Linux system I am using.

## DevPod
[Dev containers](https://containers.dev/) were designed to work with VSCode. Since I don't use VSCode on my personal machines and prefer to use Neovim, I needed a solution to run them without being locked into a vendor / IDE.

[DevPod](https://devpod.sh/) is an open source tool for running dev containers with any IDE. It makes it very easy to SSH into the container so that you can use a terminal-based editor such as Neovim.

## Usage
```bash
devpod up . --dotfiles https://github.com/rmjhynes/dotfiles --dotfiles-script scripts/setup.sh
```

## Features
Dev containers have many [Features](https://containers.dev/features) available that you can use in place of packages. The following features are installed in my spec:
- **aws-cli** - AWS Command Line Interface
- **go** - Go programming language
- **nix** - Nix package manager for additional packages as needed

## Persistent Storage
To preserve data across container rebuilds, the following directories are mounted as Docker volumes:
- `~/.ssh` - SSH keys and configuration
- `~/.gnupg` - GPG keys and configuration
- `~/repos` - Project repositories

## VSCode Configuration
Since I do still use VSCode for larger projects, I have configured the settings and declared the extensions that I like in the `.devcontainer/devcontainer.json` spec.
