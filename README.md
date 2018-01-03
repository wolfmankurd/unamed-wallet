Really basic example

JQuery to access electrum-vtc RPC

![screenshot](screenie.png)

Start like so

Make sure to backup your wallets from ~/.electrum-vtc

```
mkdir wallet/req
electrum-vtc create
electrum-vtc setconfig url_rewrite "['file:///`pwd`/wallet/', 'http://localhost:8000/']"
electrum-vtc setconfig requests_dir `pwd`/wallet/req
electrum-vtc daemon start
electrum-vtc load_wallet
cd wallet
python -m SimpleHTTPServer
```

We intend to be compatible with nativefier and a desktop app can be built like so

```
nativefier "http://localhost:8000/"
```
