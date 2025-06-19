# n8n Domain Enumeration Setup Guide

## 🚀 Installation & Setup

### 1. Install n8n

Choose your preferred installation method:

```bash
# Method 1: Global npm install (recommended)
npm install n8n -g

# Method 2: Docker (isolated environment)
docker run -it --rm --name n8n -p 5678:5678 n8nio/n8n

# Method 3: npx (no installation required)
npx n8n
```

### 2. Start n8n

```bash
# If installed globally
n8n start

# Access via browser
open http://localhost:5678
```

## 📥 Import Workflows

### Step 1: Download Workflow Files
- Navigate to the `workflows/` directory
- Download the JSON files you want to use

### Step 2: Import in n8n
1. Open n8n web interface
2. Click "Import from file" or "+" → "Import from file"
3. Select the downloaded JSON file
4. Click "Import"

### Step 3: Configure Workflows
1. Review imported nodes
2. Set up credentials (if required)
3. Test with safe domains

## 🔑 API Configuration (Optional)

For enhanced functionality, configure these APIs:

### SecurityTrails API
1. Sign up at [SecurityTrails](https://securitytrails.com/corp/api)
2. Get free API key (100 queries/month)
3. In n8n: Settings → Credentials → Add → "HTTP Header Auth"
4. Name: `APIKEY`, Value: `YOUR_API_KEY`

### Shodan API
1. Create account at [Shodan](https://account.shodan.io/)
2. Get API key from account page
3. Configure in n8n credentials

## ✅ Testing Your Setup

### Test with Basic Workflow
1. Import `domain-enumeration-basic.json`
2. Execute with a domain you own
3. Verify results are generated

### Example Test Domains
- Your personal website
- Test domains like `example.com`
- Domains you have permission to test

## 🔧 Troubleshooting

### Common Issues

**Workflow Import Fails**
- Check JSON syntax
- Ensure n8n version compatibility
- Try importing individual nodes

**API Rate Limiting**
- Add delays between requests
- Use fewer concurrent connections
- Monitor API quotas

**Timeout Errors**
- Increase timeout values
- Split large domain lists
- Use pagination for results

## 🔐 Security Best Practices

### Legal Compliance
- Only scan domains you own
- Get written permission for third-party domains
- Respect rate limits and robots.txt

### Data Protection
- Store API keys securely
- Don't log sensitive information
- Use HTTPS for all requests

### Rate Limiting
```javascript
// Add delays in Code nodes
await new Promise(resolve => setTimeout(resolve, 1000));
```

## 📊 Monitoring & Maintenance

### Regular Tasks
- Update API keys before expiration
- Monitor workflow execution logs
- Review and update domain lists
- Check for n8n updates

### Performance Optimization
- Monitor execution times
- Optimize node configurations
- Use caching when appropriate
- Clean up old execution data

## 🆘 Getting Help

- [n8n Documentation](https://docs.n8n.io/)
- [n8n Community Forum](https://community.n8n.io/)
- [GitHub Issues](https://github.com/Hanimn/Security-Automation-Labs/issues)