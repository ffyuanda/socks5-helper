socks5-helper - a tiny ss-local helper shell script
=========================================================

socks5-helper is a tiny [ss-local](https://github.com/shadowsocks/shadowsocks-libev) helper shell script
intended to ease the process of initiating a socks5 proxy.

## Config

0. Make sure you have `ss-local` installed, if not, consult [ss-local](https://github.com/shadowsocks/shadowsocks-libev).

1. Move the `socks5` script into your favourite bin directory (e.g. `$HOME/bin`).

2. Make sure your bin directory can be sourced to be included in `$PATH`.  

    e.g. put something like this in `$HOME/.profile` or `$HOME/.bash_profile`
    ```shell
    # set PATH so it includes user's private bin if it exists
    if [ -d "$HOME/bin" ] ; then
        PATH="$HOME/bin:$PATH"
    fi
    ```

3. Source the god-blessing `$HOME/.profile` or `$HOME/.bash_profile`.

4. Edit the `config.json` file in this repo and fill in correct info.

5. Edit the `socks5` script, find the CONFIG variable, change it to locate your `config.json` file, you are smart enough to do that.

6. Done.

## Usage

`. socks5 [init|kill]`  

Hint: don't forget the sourcing operator (the dot).

## Options

### init

inits the service and performs a connection check to google.com

### kill
kills the service

