# headscale-ecs

A self-hosted Headscale (open-source Tailscale control plane) deployed on AWS ECS Fargate. Containerised via Docker and infrastructure managed with Terraform.

`headscale/` is a git submodule pointing to [juanfont/headscale](https://github.com/juanfont/headscale).
- Clone with submodule included: `git clone --recurse-submodules https://github.com/ei-sei/headscale-aws.git`
- Or if already cloned:   `git submodule update --init`

## Local setup

**Prerequisites:** Go [version: 1.26.3]

Start control server:
```
cd headscale
make dev-server
```

Verify it is working:

```bash
curl http://127.0.0.1:8080/health
```