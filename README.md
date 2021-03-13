# WireGuard VPN template

WireGuard configs, scripts, keys, etc.

## Layout

Server configs are placed inside `./server`.

Client configs are generated in `./server/<server-name>/client`.

Helper scripts go in `./script`.

## Initial setup

``` sh
git clone git@github.com:tzvetkoff/wireguard-template.git
cd wireguard-template
rm -rf .git
git init
```

## Creating a new server

``` sh
./script/mkserver wg0 wireguard.example.org
```

## Destroying a server

```
./script/rmserver wg0
```

## Adding a new client

``` sh
./script/mkclient wg0 ClientName
```

## Removing a rogue client

``` sh
./script/rmclient wg0 ClientName
```
