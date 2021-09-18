# Docker image for Azure devops agent
 
 The image is based of the following article:
 https://docs.microsoft.com/en-us/azure/devops/pipelines/agents/docker?view=azure-devops#linux

 To build and push the image use the following command:
```
docker build -t odiovock/akash-azure-devops-agent:0.1.0 .
docker push odiovock/akash-azure-devops-agent:0.1.0
```
## Environment Variables

| Name | Description                                                 |
|----------------------|-------------------------------------------------------------|
| AZP_URL              | The URL of the Azure DevOps or Azure DevOps Server instance. |
| AZP_TOKEN            | [Personal Access Token (PAT)](../../organizations/accounts/use-personal-access-tokens-to-authenticate.md) with **Agent Pools (read, manage)** scope, created by a user who has permission to [configure agents](pools-queues.md#creating-agent-pools), at `AZP_URL`.    |
| AZP_AGENT_NAME       | Agent name (default value: the container hostname).          |
| AZP_POOL             | Agent pool name (default value: `Default`).                  |
| AZP_WORK             | Work directory (default value: `_work`).                     |