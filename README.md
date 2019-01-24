# waterfurnace-proxy
A rest proxy for controlling the waterfurnace through the symphony website

# Installation
1. Clone the repository
2. Install the dependency packages

```npm install```
3. Copy config.json.example to config.json

```cp config.json.example config.json```
4. Edit config.json and fill in the appropriate values
5. Run the proxy

```node waterfurnace-proxy.js```

# Usage
Configuration, status, and energy information is available through a GET request to /:

```curl http://localhost:3001/```

Parameters can be set through a GET request with query parameters to /:

```curl http://localhost:3001/?heatingsp_write=72```

Multiple parameters can be set in a single request:
```curl http://localhost:3001/?heatingsp_write=72&coolingsp_write=76&activemode_write=1```

# Examples
See ```examples/openhab``` for an example of openhab items and an http binding configuration to use the proxy
