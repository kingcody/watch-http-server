# watch-http-server: a command-line http server

`watch-http-server` is a simple, zero-configuration command-line http server.

It simply injects a very small javascript include right before the body tag of your HTML documents, whereby
a websocket connection is made on the host, triggering a reload of the page. Currently this happens when
any item in the folder changes but it may soon be made to be specific relevant to the loaded document.

# Installing globally:

Installation via `npm`.  If you don't have `npm` yet:

     curl https://npmjs.org/install.sh | sh

Once you have `npm`:

     npm install -g watch-http-server

This will install `watch-http-server` globally so that it may be run from the command line.

## Usage:

     watch-http-server [path] [options]
     (or alternatively, whs or watchhttpserver)

`[path]` defaults to `./public` if the folder exists, and `./` otherwise.

## Usage

### Starting watch-http-server locally

     node bin/watch-http-server

*Now you can visit http://localhost:8080 to view your server*

## Available Options:

`-p` Port to use (defaults to 8080)

`-a` Address to use (defaults to 0.0.0.0)

`-d` Show directory listings (defaults to 'True')

`-i` Display autoIndex (defaults to 'True')

`-e` or `--ext` Default file extension if none supplied (defaults to 'html')

`-s` or `--silent` Suppress http log messages from output

`-q` or `--quiet` Suppress program log messages from output

`--cors` Enable CORS via the `Access-Control-Allow-Origin` header

`-o` Open browser window after staring the server

`-S` or `--ssl` Enable https.

`-C` or `--cert` Path to ssl cert file (default: cert.pem).

`-K` or `--key` Path to ssl key file (default: key.pem).

`-h` or `--help` Print this list and exit.
