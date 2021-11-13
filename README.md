# query-skhd
A shell script to parse and output your [skhd](https://github.com/koekeishiya/skhd) config as JSON.

## Features

Parses your skhd config as described [here](https://github.com/koekeishiya/skhd/blob/b659b90576cf88100b52ca6ab9270d84af7e579b/README.md).

-  Putomatically finds the location of the skhd config file.
-  Parses the `.load` directive recursively (up to a depth of 10).
-  Parses mode definitions.
-  Parses shorcuts.
-  Parses shorcuts that are part of a mode.
-  Shows `->` and `@` when used.
-  Returns the data as JSON to be used with [jq](https://github.com/stedolan/jq) or other JSON parsing utilities.
-  Does not support querying the `.blacklist` directive yet.
-  Does not support application specific hotkeys yet.

## Installation

Download the `query_skhd` file by cloning this repository:
```sh
git clone https://github.com/es183923/query-skhd.git
```
or by directly downloading the `query_skhd` file itself [here](https://raw.githubusercontent.com/es183923/query-skhd/main/query_skhd).

## Usage

1. Add the execute permission to the file.
```sh
chmod +x query_skhd
```
2. Add the file to your `PATH`.
3. Run `query_skhd` by typing `query_skhd`

## Arguments

### Depth

Sets the depth for recursively parsing the config file.
examples:
```sh
query_skhd -d3
query_skhd -d 3
query_skhd --depth 3
query_skhd --depth3
query_skhd --depth=3
```
## Credits
This project was created as a utility for [skhd](https://github.com/stedolan/jq).
