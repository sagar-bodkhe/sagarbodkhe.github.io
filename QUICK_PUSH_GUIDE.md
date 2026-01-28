# Quick Guide: Push Your Code to GitHub

## You DON'T need a GitHub App - Just a Personal Access Token!

### Simple Steps:

1. **Go to this exact link:**
   ```
   https://github.com/settings/tokens
   ```

2. **Click "Generate new token" → "Generate new token (classic)"**

3. **Fill in:**
   - Note: `Portfolio Push`
   - Expiration: Choose your preference (or No expiration)
   - **Check the box: `repo`** (this gives you full repository access)

4. **Click "Generate token" at the bottom**

5. **COPY THE TOKEN** (it looks like: `ghp_xxxxxxxxxxxxxxxxxxxx`)

6. **Come back here and run:**
   ```bash
   git push -u origin main
   ```

7. **When prompted:**
   - Username: `sagar-bodkhe`
   - Password: **Paste your token** (not your GitHub password!)

---

## That's it! Your code will be pushed.

Your site will be live at: **https://sagarbodkhe.github.io**

---

## Still having trouble?

- Make sure you're logged into GitHub as `sagar-bodkhe` account
- The token must have `repo` scope checked
- Use the token as password, not your GitHub password
