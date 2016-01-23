# hamba
Alpine based docker image running haproxy to create a load balanceing proxy
usage: `docker run [-e MAXCONN=<max_connections>] -p <host_port>:<container_port> vadio/hamba <container_port> <backend_ip_1> <backend_port_1> <backend_ip_2> <backend_port_2> .... <backend_ip_n> <backend_port_n>

## Configuration options
- maxconn: default 32, set with environment variable MAXCONN
