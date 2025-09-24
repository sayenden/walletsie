# Walletsie.com Deployment Guide

## Google Cloud Project Setup

### 1. Project Created
- **Project ID**: `walletsie-io-project`
- **Project Name**: Walletsie
- **Status**: Created ✅

### 2. Required Setup Steps

#### Enable Billing (Required)
```bash
# Go to Google Cloud Console
# Navigate to Billing → Link a billing account
# Or use: https://console.cloud.google.com/billing
```

#### Create App Engine Application
```bash
gcloud app create --region=us-central --project=walletsie-io-project
```

#### Deploy Website
```bash
cd ~/walletsie-website
gcloud app deploy --project=walletsie-io-project
```

### 3. Domain Configuration

#### Custom Domain Setup
```bash
# Add custom domain
gcloud app domain-mappings create walletsie.com --project=walletsie-io-project

# Verify domain ownership in Google Search Console
# Add DNS records as instructed by Google Cloud
```

#### DNS Records (Add to your domain registrar)
```
# A Records (IPv4)
216.239.32.21
216.239.34.21
216.239.36.21
216.239.38.21

# AAAA Records (IPv6)
2001:4860:4802:32::15
2001:4860:4802:34::15
2001:4860:4802:36::15
2001:4860:4802:38::15

# CNAME for www
www.walletsie.com → ghs.googlehosted.com
```

## Current Status

### ✅ Completed
- [x] Google Cloud project created
- [x] App Engine API enabled
- [x] Website files prepared with Walletsie branding
- [x] Updated all meta tags and content

### ⏳ Pending
- [ ] Billing account setup
- [ ] App Engine application creation
- [ ] Initial deployment
- [ ] Custom domain mapping
- [ ] DNS configuration

## Quick Deploy Commands

```bash
# Set project
gcloud config set project walletsie-io-project

# Deploy (after billing is set up)
cd ~/walletsie-website
gcloud app deploy

# View deployed site
gcloud app browse
```

## Files Updated
- `index.html` - Updated all Agentsie → Walletsie branding
- `app.yaml` - Ready for deployment
- All meta tags updated for walletsie.com

## Next Steps
1. Set up billing in Google Cloud Console
2. Create App Engine application
3. Deploy website
4. Configure custom domain
5. Update DNS records
