# gh-ssh-allowed-signers

A `gh` extension to generate SSH allowed users file from GitHub users' signing keys.

## Quickstart

1. `gh extension install andyfeller/gh-ssh-allowed-signers`
1. `gh ssh-allowed-signers <organization>/<team>`
1. Profit! :moneybag: :money_with_wings: :money_mouth_face: :money_with_wings: :moneybag:

## Usage

`gh-ssh-allowed-signers` extension will create and populate `~/.ssh/allowed_signers` file with public signing keys for users individually or all users within a GitHub team.

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
  -o, --output-file <output-file>     Path to SSH allowed signers file to generate; default '/Users/andyfeller/.ssh/allowed_signers'
```

The resulting SSH allowed signers file will contain all of the public signing keys for each user with the principal based on the user's GitHub no reply email address.  For example, here is the result if you executed `gh ssh-allowed-signers andyfeller`:

```shell
andyfeller@users.noreply.github.com ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAILGK6uBGvfjK+DGqiDguxDFUoScNC/hwKQ02clco0nz8
andyfeller@users.noreply.github.com ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIALqMCzXle3FO/oaOIyxkmutYphiZ8TH+udmH4Mc/a1V
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
