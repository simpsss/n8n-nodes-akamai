# n8n-nodes-akamai

[![npm version](https://img.shields.io/npm/v/n8n-nodes-akamai.svg)](https://www.npmjs.com/package/n8n-nodes-akamai)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![n8n Community Node](https://img.shields.io/badge/n8n-Community%20Node-FF6D5A.svg)](https://n8n.io)

Professional Akamai API integration for n8n workflows with automatic EdgeGrid authentication.

## Features

- Automatic EdgeGrid authentication handling
- Complete REST API support (GET, POST, PUT, DELETE)
- PAPI-Use-Prefixes header management
- Custom headers and query parameters
- Comprehensive error handling
- Structured response data with status codes and headers

## Prerequisites

- n8n v1.104.2+ (self-hosted installation required)
- Active Akamai account with API access

## Installation

### Step 1: Enable Community Nodes

Configure your n8n instance to support Community Nodes:

```yaml
# docker-compose.yml
services:
  n8n:
    image: n8nio/n8n:latest
    environment:
      - N8N_COMMUNITY_PACKAGES_ENABLED=true
      - N8N_REINSTALL_MISSING_PACKAGES=true
```

### Step 2: Install Package

1. Navigate to **Settings → Community Nodes** in your n8n instance
2. Click **Install** and enter: `n8n-nodes-akamai`
3. Restart n8n to complete installation

## Authentication

### API Credentials Setup

1. Access **Identity & Access Management → API clients** in Akamai Control Center
2. Create or configure API client with required permissions
3. Note your credentials for n8n configuration

### n8n Credentials Configuration

Create **Akamai API** credentials with:

| Field | Description |
|-------|-------------|
| Client Token | API client token |
| Client Secret | API client secret |
| Access Token | API access token |
| Host | API hostname (e.g., `akab-xxxxx.luna.akamaiapis.net`) |

## Configuration

### PAPI Use Prefixes

| Option | Behavior |
|--------|----------|
| Don't Send Header | Use client default |
| Include Prefixes (True) | Include ID prefixes (prp_, ctr_, grp_) |
| Remove Prefixes (False) | Return clean IDs |

### Response Format

**Success Response:**
- HTTP status code and headers
- Response body data
- Request endpoint information

**Error Response:**
- Error details and status code
- Complete response data
- Original request information

## Support

- [GitHub Issues](https://github.com/simpsss/n8n-nodes-akamai/issues)
- [Akamai Developer Documentation](https://techdocs.akamai.com/developer/docs)
- [n8n Community Forum](https://community.n8n.io)

## License

MIT License - see [LICENSE.md](LICENSE.md) for details.

## About

Community node providing integration between n8n automation workflows and Akamai's API ecosystem.
