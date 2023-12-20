# Tutorial resources for: Deploy self-hosted CI/CD runners and agents with Azure Container Apps jobs

See the [tutorial](https://learn.microsoft.com/azure/container-apps/tutorial-ci-cd-runners-jobs) for more information.

## Run the Azure DevOps Agent Locally

```bash
docker build -t ado-agent:latest -f Dockerfile.azure-pipelines .
```

```bash
docker run -e AZP_URL="<AZURE_DEVOPS_ORG_URL>" -e AZP_TOKEN="<AZURE_DEVOPS_PAT>" -e AZP_POOL="<AZURE_DEVOPS_AGENT_POOL>" ado-agent:latest
```