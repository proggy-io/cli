# Proggy CLI

The Proggy CLI tool is the companion software application to [Proggy](https://proggy.io). With the CLI tool, you can run your Prog commands (built on Proggy).

## Installation

There are two methods to install the Proggy CLI tool:

1. With a package manager for your platform (Recommended)
2. Manually

### Package Manager Installation

The Proggy CLI tool can be installed using popular package manager solutions for Linux, macOS, and Windows. For specific instructions, please refer to the section for your specific platform.

### Linux

```bash
curl -s https://apt.proggy.io/proggy.asc | sudo tee /etc/apt/trusted.gpg.d/proggy.asc > /dev/null && echo "deb https://apt.proggy.io stable main" | sudo tee /etc/apt/sources.list.d/proggy.list && sudo apt update && sudo apt install proggy
```

### macOS

```bash
brew install proggy-io/proggy/proggy
```

### Windows

```bash
choco install proggy
```

## Authenticating the CLI tool

Once installed, you will need to authenticate your Proggy CLI installation. To do this, you will need a Proggy account.

### If you do not have an account

You can create a Proggy account on the web on our [sign up page](https://proggy.io/sign_up), or you can type `proggy register` in your shell after you have installed the CLI tool.

### Authentication

Once you have an account, you can login with `proggy login`. If you are on an environment where a browser is installed, Proggy will attempt to open the URL in a new window where you can login and authenticate the CLI tool.

If you are installing Proggy in a terminal-based environment (ie. Ubuntu server-only installation), you will need to create an authentication token (using the web on a separate computer) and authenticate using the following command:

```bash
proggy login --token <your token>
```

## Usage

After authentication, you can execute any commands available to you using the syntax:

```bash
proggy run <command name>
```

For detailed instructions on the available options, refer to our [documentation on running commands](https://proggy.io/docs/running-prog).

Example:

```bash
proggy run official/joke
```

## License

Please refer to the [LICENSE.md](https://github.com/proggy-io/cli/blob/main/LICENSE.md) file.

(c) Copyright 2024 Proggy
