# SSL Expiry API 🚀

A minimal Cloudflare Worker that returns SSL certificate details for any domain in JSON:

- **issuer**: Certificate Authority (CA) name  
- **valid_to**: Expiration date (ISO 8601)  
- **days_left**: Days remaining until expiry  

---

## Usage

No API key required. Simply make an HTTP GET request:

GET https://ssl-check2.talben123.workers.dev/?host=example.com


### Example Response

```json
{
  "host": "example.com",
  "issuer": "Let’s Encrypt R3",
  "valid_to": "2025-04-30T23:59:59Z",
  "days_left": 370
}

{ 
  "error": "no certificate data found" 
}


Development

git clone https://github.com/talben123/ssl-expiry-api.git
cd ssl-expiry-api
npm install -g wrangler
wrangler publish

“This project is licensed under the MIT License. See LICENSE for details.”

