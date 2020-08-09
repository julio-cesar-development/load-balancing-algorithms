# Load Balancing Algorithms

## [Nginx](https://docs.nginx.com/nginx/admin-guide/load-balancer/http-load-balancer/)

* [Nginx - Round Robin (Default)](./nginx/round_robin)
* [Nginx - Weighted Round Robin](./nginx/round_robin_weight)
* [Nginx - Least Connection](./nginx/least_connection)
* [Nginx - Weighted Least Connection](./nginx/least_connection_weight)
* [Nginx - IP Hash (Sticky Session)](./nginx/ip_hash)
* [Nginx - Random](./nginx/random)

## [Envoy Proxy](https://www.envoyproxy.io/docs/envoy/latest/intro/arch_overview/upstream/load_balancing/load_balancers/)

* [Envoy - Round Robin](./envoy/round_robin)
* [Envoy - Least Connection(request)](./envoy/least_connection)
* [Envoy - Maglev](./envoy/maglev)
* [Envoy - Ring Hash](./envoy/ring_hash)
* [Envoy - Random](./envoy/random)

## [HAProxy](https://cbonte.github.io/haproxy-dconv/1.8/configuration.html#4.2-balance)

* [HAProxy - Round Robin](./haproxy/round_robin)
* [HAProxy - Least Connection](./haproxy/least_connection)

### Running

```bash
cd ${WEB_SERVER}/${ALGORITHM}
docker-compose up --force-recreate
```

### Tests

```bash
while true; do
  curl http://localhost:8000/api/v1/
done
```

### License

This project is [MIT](LICENSE) licensed.
