# Vision

## Context

fly.io is a friendly platform available as a service. It provides excellent features like:

- building containers
- deployment
- external routing
  - automatic TLS
  - automatic load balancer
- internal routing between different apps

fly.io runs applications on top of microvms (firecracker), which is a superior technology. 
It provides excellent isolation and provides a high level of security.

The closest offering right now is Heroku, which also provides most of the same features.

Rancher RIO: TBD

## Gaps

- Both alternatives are closed source, meaning you can not install any of these alternatives in your infrastructure.
- Rancher RIO is open source but it is tied to Kubernetes.
- Waypoint has a great abstraction to deploy in most common used platforms, but it lacks in vendor locking with hcl config file, and it's still beta (v0.2.2).
- Heroku, Gcloud (GAE) great tools but you can only deploy one service.
- Kubevela is an open source PaaS for kubernetes only.


## Approach to fill the Gap

TBD

----

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
- Independence of infrastructure, MVP with docker-compose or docker-swarm
- Can deploy the services you want inside a cluster. Heroku and GAE only offers deploying one service

#### Tools & take a look at

- Logging:
  - https://github.com/apex/log
  - https://github.com/rs/zerolog
- Docker & docker-compose SDK: 
  - https://docs.docker.com/engine/api/sdk/
  - https://github.com/docker/cli/tree/master/cli/compose
- Cli creation:
  - https://github.com/urfave/cli/blob/master/docs/v2/manual.md
  - https://github.com/spf13/cobra
- Toml management
  - https://github.com/toml-lang/toml/wiki