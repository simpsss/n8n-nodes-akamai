# n8n-nodes-akamai

Akamai API integration for n8n workflows.  
_Developed by an Akamai partner_

---

## Prerequisites

- Active **Akamai** account
- Permission to create **API credentials**
- **n8n v1.104.2** or newer (**self‑hosted only**; Community Nodes are not available on n8n Cloud)

---

## Environment Variables

To enable Community Nodes support and ensure external packages like `n8n-nodes-akamai` work correctly, set the following environment variables in your n8n instance:

- `N8N_COMMUNITY_PACKAGES_ENABLED=true`  
  Enables Community Nodes feature.

- `N8N_REINSTALL_MISSING_PACKAGES=true`  
  Automatically reinstalls missing packages on startup.

If you run n8n with Docker, your `docker-compose.yml` snippet may look like this:

```yaml
services:
  n8n:
    image: n8nio/n8n:latest
    environment:
      - N8N_COMMUNITY_PACKAGES_ENABLED=true
      - N8N_REINSTALL_MISSING_PACKAGES=true
      # other environment variables...
    # volumes, ports, etc.
```

---

## Installation

Install via **n8n's Community Nodes**:

1. Go to **Settings → Community Nodes** in your n8n instance.
2. Click **Install**.
3. Enter:
   ```
   n8n-nodes-akamai
   ```
4. ⚠️ **Restart n8n** (required for external dependencies).

---

## Configuration

Create **Akamai** credentials with:

- **Client Token** – Your client token
- **Client Secret** – Your client secret
- **Access Token** – Your access token
- **Host** – Your API host (e.g. `akab-xxxxx.luna.akamaiapis.net`)

Obtain these credentials from the **Akamai Control Center** under **Identity & Access Management**.

---

## Usage

The node supports GET and POST requests to any Akamai API endpoint.

---

## About

This community node was developed by an **Akamai partner** to enable seamless integration between n8n workflows and Akamai's **EdgeGrid APIs**.  
It automatically handles all required **EdgeGrid authentication**.

---

## Support

For issues or feature requests, please open an issue on the GitHub repository.

---

## License

MIT
