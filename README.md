# 🚀 n8n-nodes-akamai

[![npm version](https://img.shields.io/npm/v/n8n-nodes-akamai.svg)](https://www.npmjs.com/package/n8n-nodes-akamai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![n8n Community Node](https://img.shields.io/badge/n8n-Community%20Node-FF6D5A.svg)](https://n8n.io)

**Professional Akamai API integration for n8n workflows**

Seamlessly integrate Akamai's powerful APIs into your n8n automation workflows with automatic EdgeGrid authentication. Built by Akamai partners for enterprise-grade reliability.

---

## ✨ Features

- 🔐 **Automatic Authentication** - Seamless EdgeGrid signature handling
- 🌐 **Full API Coverage** - Support for all Akamai REST APIs (GET, POST, PUT, DELETE)
- ⚡ **Smart Prefixes Control** - Built-in PAPI-Use-Prefixes header management
- 🎯 **Flexible Parameters** - Custom headers and query parameters support
- 🔄 **Error Resilience** - Comprehensive error handling with detailed responses
- 📊 **Rich Responses** - Structured output with status codes, headers, and body data

---

## 🛠️ Prerequisites

| Requirement | Version/Details |
|-------------|----------------|
| **n8n** | v1.104.2+ (self-hosted only) |
| **Node.js** | 20.15+ |
| **Akamai Account** | Active with API access |

> ⚠️ **Note**: Community Nodes are not available on n8n Cloud. Self-hosted installation required.

---

## 📦 Installation

### Method 1: n8n Community Nodes (Recommended)

1. Navigate to **Settings → Community Nodes** in your n8n instance
2. Click **Install** and enter:
   ```
   n8n-nodes-akamai
   ```
3. **Restart n8n** to activate external dependencies

### Method 2: Environment Setup

Ensure your n8n instance has Community Nodes enabled:

```yaml
# docker-compose.yml
services:
  n8n:
    image: n8nio/n8n:latest
    environment:
      - N8N_COMMUNITY_PACKAGES_ENABLED=true
      - N8N_REINSTALL_MISSING_PACKAGES=true
```

---

## 🔑 Authentication Setup

### 1. Create API Credentials in Akamai Control Center

1. Go to **Identity & Access Management → API clients**
2. Create a new API client or use existing credentials
3. Ensure your client has appropriate API permissions

### 2. Configure n8n Credentials

Create new **Akamai API** credentials with:

| Field | Description |
|-------|-------------|
| **Client Token** | Your API client token |
| **Client Secret** | Your API client secret |
| **Access Token** | Your API access token |
| **Host** | Your API hostname (e.g., `akab-xxxxx.luna.akamaiapis.net`) |

---

## 📋 Supported Operations

| Operation | Method | Use Case |
|-----------|--------|----------|
| **GET Request** | `GET` | Retrieve data, list resources |
| **POST Request** | `POST` | Create new resources |
| **PUT Request** | `PUT` | Update existing resources |
| **DELETE Request** | `DELETE` | Remove resources |

---

## 🎛️ Advanced Configuration

### PAPI Use Prefixes Options

| Option | Description |
|--------|-------------|
| **Don't Send Header** | Use client default setting |
| **Include Prefixes (True)** | Include ID prefixes (prp_, ctr_, grp_) |
| **Remove Prefixes (False)** | Return clean IDs without prefixes |

### Response Structure

Successful responses include:
- Success status and error flags
- HTTP status code and headers
- Response body data
- Request endpoint information

Error responses include:
- Detailed error information
- HTTP status code and headers
- Full response data for debugging
- Original request details

---

## 🤝 Contributing

Contributions are welcome!

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

---

## 🆘 Support

- **Issues**: [GitHub Issues](https://github.com/simpsss/n8n-nodes-akamai/issues)
- **Documentation**: [Akamai Developer Docs](https://techdocs.akamai.com/developer/docs)
- **Community**: [n8n Community Forum](https://community.n8n.io)

---

## 🏷️ About

**Developed by Akamai Partners**

This community node was created by certified Akamai partners to provide seamless integration between n8n automation workflows and Akamai's comprehensive API ecosystem.

---

<div align="center">

[⭐ Star this repo](https://github.com/simpsss/n8n-nodes-akamai) • [🐛 Report Bug](https://github.com/simpsss/n8n-nodes-akamai/issues) • [💡 Request Feature](https://github.com/simpsss/n8n-nodes-akamai/issues)

</div>
