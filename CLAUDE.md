# Quantum Directory

This public portfolio variant is a static directory of quantum companies. Keep
the source attribution in `index.html` and do not add private research files to
the deployment branch.

## Deploy Configuration (configured by /setup-deploy)
- Platform: Dokploy
- Production URL: https://quantum.edustardynamics.cloud
- Deploy workflow: Dokploy GitHub deployment from the public-demo branch
- Deploy status command: Dokploy MCP application status
- Merge method: direct public-demo branch
- Project type: static web app
- Post-deploy health check: https://quantum.edustardynamics.cloud

### Custom deploy hooks
- Pre-merge: verify index.html renders locally
- Deploy trigger: Dokploy MCP application.deploy
- Deploy status: poll Dokploy deployment and application status
- Health check: https://quantum.edustardynamics.cloud
