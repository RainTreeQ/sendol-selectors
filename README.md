# Sendol AI Extension - Dynamic Selectors

This repository hosts the dynamic DOM selectors configuration for the Sendol AI Broadcast Extension.

## Quick Update Guide

When an AI platform changes its UI:

1. Open the platform in your browser
2. Open DevTools (F12) and find the new input field selector
3. Update `selectors.json` with the new selector
4. Commit and push

Example:
```bash
# Test the selector in DevTools console first
document.querySelector('YOUR_NEW_SELECTOR')

# If it works, update selectors.json
git add selectors.json
git commit -m "fix: update ChatGPT input selector"
git push
```

Users will automatically receive the update within 12 hours.

## File Format

```json
{
  "platformId": {
    "findInput": ["selector1", "selector2"],
    "findSendBtn": ["selector1", "selector2"]
  }
}
```

Selectors are tried in order. First match wins.
