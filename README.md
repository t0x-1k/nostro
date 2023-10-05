# NostrO
[![License: ODbL](https://img.shields.io/badge/License-PDDL-brightgreen.svg)](https://opendatacommons.org/licenses/pddl/)  [![Go Report Card](https://goreportcard.com/badge/github.com/r3drun3/nostro)](https://goreportcard.com/report/github.com/r3drun3/nostro)  [![goreleaser](https://github.com/R3DRUN3/nostro/actions/workflows/release.yaml/badge.svg)](https://github.com/R3DRUN3/nostro/actions/workflows/release.yaml)  [![Latest Release](https://img.shields.io/github/v/release/r3drun3/nostro?logo=github)](https://github.com/r3drun3/nostro/releases)

**Nostr Osint Tool** 🔎 𓅦  
  

<img src="images/logo.png" alt="Nostr Logo" width="300" height="200">  

`NostrO` is designed for conducting *Open Source Intelligence* (OSINT) operations on [Nostr](https://nostr.com/).  
NostrO facilitates operations such as retrieving relay infos, keyword search on notes filtered by user, and more.  

> **Warning**
> The tool is currently in a very early and experimental phase.

## Development
I welcome pull requests and contributions!  
This tool is a CLI implemented with [cobra](https://github.com/spf13/cobra) and [go-nostr](https://github.com/nbd-wtf/go-nostr) library.  
I suggest using `VS Code` for local development.  
For debugging you can create a `launch.json` file similar to the following (change the command you want to test):  
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Launch Package",
            "type": "go",
            "request": "launch",
            "mode": "auto",
            "program": "${workspaceFolder}/main.go", // Update the path to main.go
            "args": ["relay", "info", "bitcoinmaximalists.online"],
            "env": {},
            "showLog": true
        }
    ]
}
```  

  



## Examples

Retrieve relay info:  
```console
nostro relay info relay.nostrview.com
####################### RELAY INFO #######################
NAME:  relay.nostrview.com
DESCRIPTION:  Nostrview relay
PUB KEY:  2e9397a8c9268585668b76479f88e359d0ee261f8e8ea07b3b3450546d1601c8
CONTACT:  2e9397a8c9268585668b76479f88e359d0ee261f8e8ea07b3b3450546d1601c8
SUPPORTED NIPS:  [1 2 4 9 11 12 15 16 20 22 26 28 33 40 111]
SOFTWARE:  git+https://github.com/Cameri/nostream.git
VERSION:  1.22.2
LIMITATION:  &{524288 10 10 5000 256 4 2500 102400 0 false true}
PAYMENTSURL:  https://relay.nostrview.com/invoices
##########################################################
```  

