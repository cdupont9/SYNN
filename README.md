# SYNN — The Couple Social Network & Facebook Bridge 💍

> **SYNN** is Facebook reimagined for couples. Instead of separate accounts that tag each other, SYNN connects two individual Facebook profiles into a **merged joint presence** acting as a **smart bridge to real Facebook**.

---

## 🚀 How to Upload this Project to GitHub

This repository is already initialized with git! To upload it to your personal GitHub account:

1. Create a new repository on [GitHub](https://github.com/new) (e.g. named `SYNN`).
2. Run these commands in your terminal from `/Users/charitydupont/Desktop/SYNN`:

```bash
# Add your GitHub remote repository
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/SYNN.git

# Set the default branch to main
git branch -M main

# Push all files to GitHub
git push -u origin main
```

---

## 🌉 How the Facebook Bridge Works

Facebook's native platform only permits 1 user per personal profile. SYNN solves this with the **Facebook Bridge Engine**:

```
[Partner A Facebook Account]       [Partner B Facebook Account]
            \                             /
             \                           /
        [SYNN Facebook Bridge (Meta Graph API / OAuth)]
                         |
      ----------------------------------------
      |                                      |
[Mode 1: Post as Joint Couple]      [Mode 2: Post as Me]
  - Co-tags spouse on Facebook        - Posts to single timeline
  - Dispatches to both timelines      - Retains personal voice
  - Adds joint couple badge
```

### 1. Dual Authentication & Linking
Both partners connect their Facebook accounts via Facebook OAuth. SYNN links both Facebook User IDs to the shared couple entity.

### 2. Co-Posting & Co-Tagging
When you post as **Maya & Liam (Joint)**:
- The SYNN Bridge packages the post with joint couple attribution (`[💍 Shared Moment via SYNN: Maya & Liam]`).
- It co-tags the spouse on Facebook, ensuring the memory appears on **BOTH** partners' Facebook timelines simultaneously.

### 3. Native Facebook Share Dialog & Graph API
- Supports live Graph API v20.0 publishing with Meta App ID (`developers.facebook.com`).
- Provides deep-link share dialogs (`https://www.facebook.com/sharer/sharer.php`) so users on mobile phones can trigger native Facebook app sharing.

---

## 📱 How to Download & Run on Your Mobile Phone

SYNN is configured as an installable **Progressive Web App (PWA)** broadcasting across your local network:

1. Connect your phone to the same Wi-Fi network as your computer.
2. Open Safari (iOS) or Chrome (Android) and navigate to:
   ```
   http://172.20.224.182:5173/
   ```
3. Tap **Share** (iOS) or **Three Dots** (Android) > select **"Add to Home Screen"**.
4. The **SYNN app icon** will appear on your home screen and open in fullscreen mode.

---

## 🔑 Pre-Configured Test Accounts (Real Persistent Data)

| Profile | Email | Password | Account Type |
| :--- | :--- | :--- | :--- |
| **Maya Davis** | `maya@synn.com` | `password123` | Spouse A (Merged Joint Account) |
| **Liam Vance** | `liam@synn.com` | `password123` | Spouse B (Merged Joint Account) |
| **Marcus Chen** | `marcus@synn.com` | `password123` | Single Individual Profile |
| **Elena Rostova** | `elena@synn.com` | `password123` | Single Individual Profile |

*(All posts, comments, reactions, and marriage states persist in `localStorage` across page reloads and mobile app launches).*

---

## 🛠️ Development Scripts

```bash
# Install dependencies
npm install

# Start development server on network (0.0.0.0:5173)
npm run dev

# Build production bundle
npm run build
```
