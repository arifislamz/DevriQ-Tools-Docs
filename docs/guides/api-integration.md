# API Integration Guide

**Integrate DevriQ Tools into your applications** — Programmatic access to tool functionality via our REST API.

---

## 📚 Table of Contents

- [Getting Started](#-getting-started)
- [API Endpoints](#-api-endpoints)
- [Authentication](#-authentication)
- [Examples](#-examples)
- [Rate Limiting](#-rate-limiting)
- [Error Handling](#-error-handling)

---

## 🚀 Getting Started

### Prerequisites

- API key (request from [contact →](https://devriq.in/contact-us))
- Familiarity with REST APIs
- HTTP client (curl, Postman, etc.)
- JSON format knowledge

### API Base URL

```
https://api.tools.devriq.in/v1
```

All requests must use HTTPS.

---

## 🔑 Authentication

### API Key

Include your API key in request headers:

```
X-API-Key: your_api_key_here
```

### Example Request

```bash
curl -X POST https://api.tools.devriq.in/v1/pdf/merge \
  -H "X-API-Key: your_api_key_here" \
  -H "Content-Type: application/json" \
  -d '{...}'
```

---

## 📝 API Endpoints

### PDF Tools

#### Merge PDFs

```
POST /pdf/merge
```

**Request:**
```json
{
  "pdfs": ["base64_encoded_pdf_1", "base64_encoded_pdf_2"],
  "output_format": "application/pdf"
}
```

**Response:**
```json
{
  "status": "success",
  "result": "base64_encoded_merged_pdf",
  "size_bytes": 1024000,
  "processing_time_ms": 250
}
```

#### Compress PDF

```
POST /pdf/compress
```

**Request:**
```json
{
  "pdf": "base64_encoded_pdf",
  "quality": 85,
  "target_size_mb": null
}
```

**Response:**
```json
{
  "status": "success",
  "result": "base64_encoded_compressed_pdf",
  "original_size": 2048000,
  "compressed_size": 1024000,
  "reduction_percent": 50
}
```

### Image Tools

#### Compress Image

```
POST /image/compress
```

**Request:**
```json
{
  "image": "base64_encoded_image",
  "quality": 80,
  "format": "png"
}
```

**Response:**
```json
{
  "status": "success",
  "result": "base64_encoded_compressed_image",
  "original_size": 512000,
  "compressed_size": 256000
}
```

#### Resize Image

```
POST /image/resize
```

**Request:**
```json
{
  "image": "base64_encoded_image",
  "width": 800,
  "height": 600,
  "maintain_aspect_ratio": true,
  "format": "png"
}
```

**Response:**
```json
{
  "status": "success",
  "result": "base64_encoded_resized_image",
  "new_dimensions": {
    "width": 800,
    "height": 600
  }
}
```

### Developer Tools

#### Format JSON

```
POST /dev/json-format
```

**Request:**
```json
{
  "json": "{\"key\":\"value\",\"nested\":{\"data\":123}}",
  "minify": false,
  "indent": 2
}
```

**Response:**
```json
{
  "status": "success",
  "result": "{\n  \"key\": \"value\",\n  \"nested\": {\n    \"data\": 123\n  }\n}",
  "is_valid": true,
  "errors": []
}
```

#### Generate QR Code

```
POST /dev/qr-generate
```

**Request:**
```json
{
  "data": "https://tools.devriq.in",
  "size": 300,
  "format": "png",
  "error_correction": "M",
  "logo": null
}
```

**Response:**
```json
{
  "status": "success",
  "result": "base64_encoded_qr_image",
  "dimensions": {
    "width": 300,
    "height": 300
  }
}
```

---

## 📊 Complete Examples

### Example 1: Merge Multiple PDFs

```python
import requests
import base64

API_KEY = "your_api_key"
API_URL = "https://api.tools.devriq.in/v1/pdf/merge"

# Read PDF files
with open("file1.pdf", "rb") as f:
    pdf1 = base64.b64encode(f.read()).decode()
with open("file2.pdf", "rb") as f:
    pdf2 = base64.b64encode(f.read()).decode()

# Prepare request
payload = {
    "pdfs": [pdf1, pdf2],
    "output_format": "application/pdf"
}

headers = {
    "X-API-Key": API_KEY,
    "Content-Type": "application/json"
}

# Make request
response = requests.post(API_URL, json=payload, headers=headers)
result = response.json()

# Save result
if result["status"] == "success":
    with open("merged.pdf", "wb") as f:
        f.write(base64.b64decode(result["result"]))
    print(f"Merged PDF created ({result['size_bytes']} bytes)")
```

### Example 2: Compress Multiple Images

```javascript
const axios = require('axios');
const fs = require('fs');
const path = require('path');

const API_KEY = 'your_api_key';
const API_URL = 'https://api.tools.devriq.in/v1/image/compress';

async function compressImages(imageDir) {
  const files = fs.readdirSync(imageDir);
  
  for (const file of files) {
    if (!['.png', '.jpg', '.jpeg'].includes(path.extname(file))) {
      continue;
    }
    
    const imagePath = path.join(imageDir, file);
    const imageData = fs.readFileSync(imagePath);
    const base64Image = imageData.toString('base64');
    
    const payload = {
      image: base64Image,
      quality: 80,
      format: path.extname(file).substring(1)
    };
    
    const headers = {
      'X-API-Key': API_KEY,
      'Content-Type': 'application/json'
    };
    
    try {
      const response = await axios.post(API_URL, payload, { headers });
      
      if (response.data.status === 'success') {
        const compressed = Buffer.from(response.data.result, 'base64');
        fs.writeFileSync(
          imagePath.replace('.', '-compressed.'),
          compressed
        );
        console.log(`Compressed: ${file}`);
      }
    } catch (error) {
      console.error(`Error compressing ${file}:`, error.message);
    }
  }
}

// Usage
compressImages('./images');
```

---

## ⚙️ Rate Limiting

### Limits

- Free tier: 100 requests/hour
- Basic tier: 1,000 requests/hour
- Professional: 10,000 requests/hour
- Enterprise: Custom limits

### Response Headers

```
X-RateLimit-Limit: 1000
X-RateLimit-Remaining: 950
X-RateLimit-Reset: 1622548800
```

### Handling Rate Limits

```python
import time
from datetime import datetime

if response.status_code == 429:
    reset_time = int(response.headers.get('X-RateLimit-Reset'))
    wait_seconds = reset_time - int(datetime.now().timestamp())
    print(f"Rate limited. Waiting {wait_seconds} seconds...")
    time.sleep(wait_seconds)
```

---

## 🚨 Error Handling

### HTTP Status Codes

| Code | Meaning | Action |
|------|---------|--------|
| 200 | Success | Use result |
| 400 | Bad request | Check parameters |
| 401 | Unauthorized | Verify API key |
| 429 | Rate limited | Wait and retry |
| 500 | Server error | Retry later |

### Error Response

```json
{
  "status": "error",
  "error_code": "INVALID_PDF",
  "message": "Uploaded file is not a valid PDF",
  "details": {
    "field": "pdf",
    "reason": "Corrupted or invalid PDF header"
  }
}
```

### Retry Logic

```python
import requests
from requests.adapters import HTTPAdapter
from requests.packages.urllib3.util.retry import Retry

def create_session():
    session = requests.Session()
    retry = Retry(
        total=3,
        backoff_factor=1,
        status_forcelist=[429, 500, 502, 503, 504]
    )
    adapter = HTTPAdapter(max_retries=retry)
    session.mount('https://', adapter)
    return session

session = create_session()
response = session.post(url, json=payload, headers=headers)
```

---

## 📦 SDKs & Libraries

### Official SDKs

- **Python** → [devriq-python (PyPI)](https://pypi.org/)
- **JavaScript** → [devriq-js (NPM)](https://www.npmjs.com/)
- **Go** → [devriq-go (GitHub)](https://github.com/)

### Example: Python SDK

```python
from devriq import DevriQClient

client = DevriQClient(api_key="your_api_key")

# Merge PDFs
result = client.pdf.merge(
    pdfs=["file1.pdf", "file2.pdf"],
    output_format="pdf"
)

# Compress image
result = client.image.compress(
    image="photo.jpg",
    quality=80
)
```

---

## 📝 Webhook Callbacks

### Enable Webhooks

For long-running operations, webhooks provide completion callback:

```bash
POST /v1/webhooks/register

{
  "url": "https://yourapp.com/callback",
  "events": ["pdf.merge.complete", "image.compress.complete"]
}
```

### Webhook Payload

```json
{
  "event": "pdf.merge.complete",
  "timestamp": "2026-04-02T10:30:00Z",
  "data": {
    "request_id": "req_123456",
    "status": "success",
    "result_url": "https://api.tools.devriq.in/v1/results/res_123456"
  }
}
```

---

## 📞 Support

### API Support

- 📧 Email: [api@devriq.in](mailto:api@devriq.in)
- 📖 Docs: [api.tools.devriq.in/docs](https://tools.devriq.in/api-docs/)
- 🐛 Issues: [GitHub Issues](https://github.com/)
- 💬 Discussions: [GitHub Discussions](https://github.com/)

### Rate Limit Queries

- [Contact enterprise](https://devriq.in/contact-us)
- [Email support](mailto:support@devriq.in)
- [Upgrade tier](https://tools.devriq.in/)

---

**Last Updated**: April 2, 2026 | **API Version**: v1 | **Status**: Stable ✅

---

**Need help?** [Contact →](https://devriq.in/contact-us)  
**Have ideas?** [Share →](https://devriq.in/contact-us)  
**Found bugs?** [Report →](mailto:api@devriq.in)

---

© 2026 DevriQ Tools. All rights reserved.
