# GitHub Push Instructions

## Option 1: Use Personal Access Token (PAT) - RECOMMENDED

### Step 1: Create Token
1. Go to: https://github.com/settings/tokens
2. Click "Generate new token (classic)"
3. Name: "Task Manager Assignment"
4. Select scope: "repo" (check the box)
5. Click "Generate token"
6. COPY the token immediately!

### Step 2: Push with Token
Run this command (replace YOUR_TOKEN with the token you copied):

```bash
git push https://YOUR_TOKEN@github.com/Multimedia-and-Web-Design-L300-25-26/task-manager-rest-api-with-authentication-justice-tieku.git main
```

### Step 3: (Optional) Save credentials
To avoid entering token every time:
```bash
git config credential.helper store
git push
```
Then enter your token when prompted. It will be saved for future pushes.

---

## Option 2: Use GitHub CLI (gh)

If you have GitHub CLI installed:
```bash
gh auth login
git push origin main
```

---

## Option 3: Use SSH (More Setup Required)

1. Generate SSH key:
```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

2. Add to GitHub:
   - Copy the public key: `cat ~/.ssh/id_ed25519.pub`
   - Go to: https://github.com/settings/keys
   - Click "New SSH key" and paste

3. Change remote to SSH:
```bash
git remote set-url origin git@github.com:Multimedia-and-Web-Design-L300-25-26/task-manager-rest-api-with-authentication-justice-tieku.git
git push origin main
```

---

## Quick Fix (One-time push)

If you just need to push once right now:

```bash
git push https://justice-tieku@github.com/Multimedia-and-Web-Design-L300-25-26/task-manager-rest-api-with-authentication-justice-tieku.git main
```

When prompted for password, enter your Personal Access Token (NOT your GitHub password).

---

## Troubleshooting

If you get "nothing to commit":
```bash
git status
git add .
git commit -m "Complete Task Manager API implementation"
git push
```

If you need to check what changed:
```bash
git status
git diff
```
