# GitHub Authentication Guide

## Option 1: Personal Access Token (Recommended for HTTPS)

### Step 1: Navigate to Personal Access Tokens
1. Go to: **https://github.com/settings/tokens**
   - Or: Click your profile picture (top right) → **Settings** → Scroll down to **Developer settings** (left sidebar) → **Personal access tokens** → **Tokens (classic)**

### Step 2: Create New Token
1. Click **"Generate new token"** → **"Generate new token (classic)"**
2. Give it a name: `Portfolio Push`
3. Set expiration (or no expiration)
4. Select scopes:
   - ✅ **repo** (Full control of private repositories)
   - This gives you read/write access
5. Click **"Generate token"**
6. **COPY THE TOKEN IMMEDIATELY** - You won't see it again!

### Step 3: Push Your Code
```bash
git push -u origin main
```
When prompted:
- **Username**: `sagar-bodkhe`
- **Password**: Paste your personal access token (NOT your GitHub password)

---

## Option 2: Deploy Keys (SSH - More Secure)

**Note**: Deploy keys are typically read-only. For pushing code, you need write access.

### Step 1: Generate SSH Key
```bash
ssh-keygen -t ed25519 -C "your_email@example.com" -f ~/.ssh/github_portfolio
```

### Step 2: Add SSH Key to Repository
1. Copy your public key:
   ```bash
   cat ~/.ssh/github_portfolio.pub
   ```
2. Go to your repository: https://github.com/sagar-bodkhe/sagarbodkhe.github.io/settings/keys
3. Click **"Add deploy key"**
4. Paste your public key
5. ✅ Check **"Allow write access"** (important!)
6. Click **"Add key"**

### Step 3: Configure Git to Use SSH Key
```bash
# Add SSH key to ssh-agent
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/github_portfolio

# Update remote URL
git remote set-url origin git@github.com:sagar-bodkhe/sagarbodkhe.github.io.git

# Push
git push -u origin main
```

---

## Option 3: GitHub CLI (Easiest)

If you have GitHub CLI installed:
```bash
# Install GitHub CLI (if not installed)
# Windows: winget install GitHub.cli

# Authenticate
gh auth login

# Push
git push -u origin main
```

---

## Quick Links

- **Personal Access Tokens**: https://github.com/settings/tokens
- **Repository Deploy Keys**: https://github.com/sagar-bodkhe/sagarbodkhe.github.io/settings/keys
- **Repository Settings**: https://github.com/sagar-bodkhe/sagarbodkhe.github.io/settings

---

## Current Status

✅ Files committed locally  
✅ Remote repository configured  
⏳ Waiting for authentication to push
