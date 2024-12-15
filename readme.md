# GenWebServer

GenWebServer is a simple web server written in C to provide basic HTTP service. It serves static content from the `/data/site/` directory and logs accesses to `/data/webserver.log`.

## How to Use:

1. Send the `elfldr.elf` payload to port 9020.
2. Send the `genwebserver.elf` payload to port 9021.
3. Access the server at `http://ps5:9080` or `http://ps5:9080/index.html`.

## Credits:

- ps5-payload-sdk
