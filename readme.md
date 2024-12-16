# GenWebServer

GenWebServer is a simple web server written in C to provide basic HTTP service. 


## Features

- Static Content Hosting.
- Access Logging.
- IP Whitelisting.
- Customizable Port.

## Configuration

The server reads its settings from `/data/genwebserver/genwebserver.conf`:

```plaintext
port=8000
site_path=/data/genwebserver/site/
allowed_ips=0.0.0.0
```

### Configuration Parameters

- **port**: The port on which the server will listen (default: `8000`).
- **site_path**: The directory where the static content is hosted (default: `/data/genwebserver/site/`).
- **allowed_ips**: Comma-separated list of IPs or IP ranges (in CIDR notation) that are allowed to access the server. Set to `0.0.0.0` to allow all IPs (default: `0.0.0.0`).

### Example Configuration

```plaintext
port=9000
site_path=/home/site/
allowed_ips=192.168.1.100,192.168.1.101,192.168.2.0/24
```

This configuration:
- Runs the server on port `9000`.
- Serves content from `/home/site/`.
- Allows access only from:
  - `192.168.1.100`
  - `192.168.1.101`
  - All IPs in the `192.168.2.0/24` range.

## How to Use

1. Send the `elfldr.elf` payload to port 9020.
2. Send the `genwebserver.elf` payload to port 9021.
3. Access the server at `http://ps5:<port>` (default port: `8000`) or `http://ps5:<port>/index.html`.

## Credits

- ps5-payload-sdk

