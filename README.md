# vision

## AS-IS

- Build local Docker images
- Toml configuration files
- Console command features:
  - Get metrics (http status codes, cache hit ratio, VM service concurrency, data transfer bytes, memory and cpu usage) / healthcheck (UP or DOWN)
  - Database management and attach it to a POD
  - Authentication management (oauth, secrets, certs)
  - Autoscaling
  - Networking management
  - Display logs of the application
  - App management (deploy, suspend, destroy)
- Communication client/server using GRPC protocol buffer

## TO-BE

- Could be nice to set cron jobs as other PaaS do like GAE
- Assign CPU and memory resources
- Create your own healthchecks
- TOML config file
- Autoscaling management
- Ingress/Egress