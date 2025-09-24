# Walletsie.com

The AI agent that maximizes your credit card rewards.

## Overview

Walletsie helps you track spending, compare cards, and ensures you never leave credit card rewards on the table. Americans leave over $6B in rewards unclaimed each year - never miss a point again.

## Features

- 🤖 AI-powered spending analysis
- 💳 Smart card recommendations
- 📊 Real-time reward optimization
- 🔔 Intelligent reminders
- 📱 Mobile-friendly dashboard

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Deployment**: Google Cloud App Engine
- **Domain**: walletsie.com

## Deployment

### Google Cloud Setup
```bash
gcloud config set project walletsie-io-project
gcloud app deploy
```

### Local Development
```bash
# Serve locally
python3 -m http.server 8080
# Open http://localhost:8080
```

## Project Structure

```
walletsie-website/
├── index.html          # Main landing page
├── app.yaml           # App Engine configuration
├── DEPLOYMENT.md      # Deployment guide
└── README.md          # This file
```

## Live Site

- **Production**: https://walletsie.com
- **App Engine**: https://walletsie-io-project.uc.r.appspot.com

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - see LICENSE file for details.
