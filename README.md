# gh-ssh-allowed-signers

A `gh` extension to generate SSH allowed users file from GitHub users' signing keys.

## Quickstart

1. `gh extension install andyfeller/gh-ssh-allowed-signers`
1. `gh ssh-allowed-signers <organization>/<team>`
1. Profit! :moneybag: :money_with_wings: :money_mouth_face: :money_with_wings: :moneybag:

## Usage

```shell
$ gh ssh-allowed-signers --help

Generate SSH allowed signers file from GitHub users.

USAGE
  gh-ssh-allowed-signers [options] <organization>/<team>
  gh-ssh-allowed-signers [options] <user>

FLAGS
  -a, --append                        Append signing keys to existing SSH allowed signers file
  -d, --debug                         Enable debugging
  -f, --force                         Whether to overwrite output file if it exists
  -o, --output-file <output-file>     Path to SSH allowed signers file to generate
```

## Setup

Like any other `gh` CLI extension, `gh-ssh-allowed-signers` is trivial to install or upgrade and works on most operating systems:

- **Installation**

  ```shell
  gh extension install andyfeller/gh-ssh-allowed-signers
  ```
  
  _For more information: [`gh extension install`](https://cli.github.com/manual/gh_extension_install)_

- **Upgrade**

  ```shell
  gh extension upgrade ssh-allowed-signers
  ```

  _For more information: [`gh extension upgrade`](https://cli.github.com/manual/gh_extension_upgrade)_
