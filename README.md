# Cloudflare Purge Cache Action

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/Scalified/cloudflare-purge-cache-action/blob/master/LICENSE)
[![Release](https://img.shields.io/github/v/release/Scalified/cloudflare-purge-cache-action?style=flat-square)](https://github.com/Scalified/cloudflare-purge-cache-action/releases/latest)

## Overview

A simple GitHub Action to purge Cloudflare cache for a specific zone

## Setup

1. Get **Zone ID** from the Cloudflare dashboard
2. Create an **API Token** with the following permissions:
   - Zone:Zone:Read
   - Zone:Cache Purge:Edit
3. Store these values as GitHub secrets:
   - `CLOUDFLARE_ZONE_ID`
   - `CLOUDFLARE_EMAIL`
   - `CLOUDFLARE_API_TOKEN`

## Usage

```yaml
- name: Purge Cloudflare Cache
  uses: scalified/cloudflare-purge-cache-action@v1
  with:
    zone-id: ${{ secrets.CLOUDFLARE_ZONE_ID }}
    email: ${{ secrets.CLOUDFLARE_EMAIL }}
    api-token: ${{ secrets.CLOUDFLARE_API_TOKEN }}
```

## Inputs

| Input       | Description               | Required |
|-------------|---------------------------|----------|
| `zone-id`   | Cloudflare Zone ID        | Yes      |
| `email`     | Cloudflare Account Email  | Yes      |
| `api-token` | Cloudflare API Token      | Yes      |

---

**Made with ❤️ by [Scalified](http://www.scalified.com)**
