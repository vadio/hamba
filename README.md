# hamba
Alpine based docker image running haproxy to create a load balanceing proxy
usage: ```docker run [-e MAXCONN=<max_connections>] -p <host_port>:<container_port> vadio/hamba <container_port> <backend_ip_1> <backend_port_1> <backend_ip_2> <backend_port_2> .... <backend_ip_n> <backend_port_n>```

## Configuration options
- maxconn: set with environment variable MAXCONN
  - default 32
  - can set unlimited with 0
- timeout connect: set with environment variable TIMEOUT_CONNECT
  - default 5000ms
  - can set unlimited with 0
  - will accept differnt units (5h, 5m, 5s)
- timeout server: set with environment variable TIMEOUT_SERVER
  - default 50000ms
  - can set unlimited with 0
  - will accept differnt units (5h, 5m, 5s)
- timeout client: set with environment variable TIMEOUT_CLIENT
  - default 50000ms
  - can set unlimited with 0
  - will accept differnt units (5h, 5m, 5s)