# Walletsie.com Domain Setup Guide

## Step 1: Verify Domain Ownership

1. **Go to Google Search Console**: https://search.google.com/search-console
2. **Add Property**: Click "Add Property" → "Domain" 
3. **Enter Domain**: `walletsie.com`
4. **Verify Ownership**: Add the TXT record to your DNS

## Step 2: Add Domain Mapping (After Verification)

```bash
gcloud app domain-mappings create walletsie.com --project=walletsie-io-project
```

## Step 3: DNS Configuration

After domain mapping is created, add these DNS records to your domain registrar:

### A Records (IPv4)
```
walletsie.com → 216.239.32.21
walletsie.com → 216.239.34.21
walletsie.com → 216.239.36.21
walletsie.com → 216.239.38.21
```

### AAAA Records (IPv6)
```
walletsie.com → 2001:4860:4802:32::15
walletsie.com → 2001:4860:4802:34::15
walletsie.com → 2001:4860:4802:36::15
walletsie.com → 2001:4860:4802:38::15
```

### CNAME Record (for www)
```
www.walletsie.com → ghs.googlehosted.com
```

## Step 4: SSL Certificate

Google Cloud will automatically provision an SSL certificate once DNS is configured.

## Current Status

- ✅ Google Cloud project: `walletsie-io-project`
- ✅ App Engine deployed: https://walletsie-io-project.uc.r.appspot.com
- ⏳ Domain verification needed: walletsie.com
- ⏳ DNS configuration pending

## Quick Commands

```bash
# Check domain mapping status
gcloud app domain-mappings list --project=walletsie-io-project

# View SSL certificate status
gcloud app ssl-certificates list --project=walletsie-io-project

# Browse current site
gcloud app browse --project=walletsie-io-project
```

## Next Steps

1. **Verify domain ownership** in Google Search Console
2. **Run domain mapping command** after verification
3. **Update DNS records** at your domain registrar
4. **Wait for SSL certificate** (automatic, takes 15-60 minutes)
5. **Test**: https://walletsie.com should work!
