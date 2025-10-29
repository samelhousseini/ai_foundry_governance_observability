# ai_foundry_governance_observability
Hands-on notebooks for learning Azure AI governance, safety, and observability patterns with Azure AI Foundry services.

## Repository Contents
- `ai_content_safety/content_safety_tutorial.ipynb` – end-to-end walkthrough of Azure AI Content Safety features (text, image, multimodal, prompt shields, blocklists, protected code detection, disconnected container workflows, and custom categories).
- `ai_observability/observability.ipynb` – quick-start guide to wiring telemetry from the Microsoft Agent Framework into Azure Monitor and the Aspire OTLP dashboard.
- `requirements.txt` – consolidated Python dependencies for both notebooks.

## Quick Start
1. Create and activate a Python 3.9+ virtual environment.
2. Install dependencies: `pip install -r requirements.txt` (or install per-notebook requirements if preferred).
3. Copy `.env.sample` to `.env` and populate the required settings before running the notebooks.
4. Launch Jupyter (`jupyter notebook` or VS Code) and open the notebook you want to explore.

## Notebook Highlights
### Azure AI Content Safety Tutorial
- Covers SDK setup, authentication (API key and AAD), severity scale helpers, and batch moderation policies.
- Demonstrates text, image, and multimodal moderation plus blocklist management and policy decision logic.
- Explores advanced features: Prompt Shields, protected code detection, disconnected container usage, and custom incident categories trained from custom data.
- Includes governance callouts on cost control, data handling, and resilience (retries, logging, drift monitoring).

**Environment variables required**
- `AZURE_AI_CONTENT_SAFETY_URL`
- `AZURE_AI_CONTENT_SAFETY_KEY`

### Observability Setup Example
- Loads environment variables to connect Agent Framework telemetry to Azure Monitor and optional OTLP exporters.
- Demonstrates configuring `setup_observability` with Application Insights, OTLP, and console exporters.
- Provides a sample weather agent built with Microsoft Agent Framework to generate traces.
- Documents supporting infrastructure commands (firewall rule, Aspire dashboard container) and encourages validating telemetry in Azure AI Foundry and Aspire dashboards.

**Environment variables referenced**
- `AZURE_OPENAI_API_KEY`
- `AZURE_OPENAI_ENDPOINT`
- `AZURE_OPENAI_MODEL_NAME`
- `ENABLE_OTEL`
- `ENABLE_SENSITIVE_DATA`
- `APPLICATIONINSIGHTS_CONNECTION_STRING`
- `OTLP_ENDPOINT`

## Additional Resources
1. [Azure AI Foundry](https://ai.azure.com/)
2. [Azure AI Content Safety Documentation](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/)
3. [Azure AI Content Safety Containers](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/how-to/containers/container-overview)
4. [Azure AI Content Safety System Messages](https://learn.microsoft.com/en-us/azure/ai-foundry/openai/concepts/system-message?tabs=top-techniques)
5. [Azure AI Content Task Adherence API](https://techcommunity.microsoft.com/blog/azure-ai-foundry-blog/keeping-agents-on-track-introducing-task-adherence-in-azure-ai-foundry/4458397)
6. [Azure AI Content Safety Custom Categories](https://learn.microsoft.com/en-us/azure/ai-services/content-safety/concepts/custom-categories?tabs=standard)
7. [Azure AI Content Safety SDK for Python](https://azuresdkdocs.z19.web.core.windows.net/python/azure-ai-contentsafety/1.0.0/index.html)
