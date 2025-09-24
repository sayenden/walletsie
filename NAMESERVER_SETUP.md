# Walletsie.com Nameserver Setup

## ✅ Google Cloud DNS Zone Created

**DNS Zone**: `walletsie-zone`
**Project**: `walletsie-io-project`

## 🌐 Nameservers to Set at Your Domain Registrar

Update your domain registrar (where you bought walletsie.com) with these nameservers:

```
ns-cloud-a1.googledomains.com
ns-cloud-a2.googledomains.com
ns-cloud-a3.googledomains.com
ns-cloud-a4.googledomains.com
```

## 📋 DNS Records Already Configured

✅ **A Records** (walletsie.com):
- 216.239.32.21
- 216.239.34.21
- 216.239.36.21
- 216.239.38.21

✅ **CNAME Record** (www.walletsie.com):
- ghs.googlehosted.com

## 🚀 Next Steps

1. **Go to your domain registrar** (GoDaddy, Namecheap, etc.)
2. **Find DNS/Nameserver settings**
3. **Replace existing nameservers** with the Google Cloud ones above
4. **Wait 24-48 hours** for DNS propagation
5. **Then run domain mapping**:
   ```bash
   gcloud app domain-mappings create walletsie.com --project=walletsie-io-project
   ```

## 🔍 Check DNS Status

```bash
# Check if DNS is propagated
dig walletsie.com
nslookup walletsie.com

# Check Google Cloud DNS records
gcloud dns record-sets list --zone=walletsie-zone --project=walletsie-io-project
```

## 📍 Current Status

- ✅ Google Cloud DNS zone created
- ✅ A records and CNAME configured
- ⏳ Nameservers need to be updated at registrar
- ⏳ Domain mapping pending DNS propagation

## 🌐 Where to Update Nameservers

**Common Registrars:**
- **GoDaddy**: Domain Manager → DNS → Nameservers
- **Namecheap**: Domain List → Manage → Nameservers
- **Google Domains**: DNS → Name servers
- **Cloudflare**: DNS → Records (if using Cloudflare)

After updating nameservers, walletsie.com will point to your Google Cloud site!
