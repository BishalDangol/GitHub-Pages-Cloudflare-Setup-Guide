# GitHub Pages + Cloudflare Setup Guide

Easily host your static website **for free** using **GitHub Pages**, and secure it with **Cloudflare** using your **custom domain**.

---

##  Pre-requirements

Before you start, make sure you have the following ready:

-  **Cloudflare account**  
-  **GitHub account**  
-  **Custom domain** connected to Cloudflare  
-  **Interest in learning through video tutorials** (recommended)

---

##  Step-by-Step Setup

###  Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) → click **New Repository**.  
2. Enter any name you like (e.g., `my-website`).  
3. Choose **Public** visibility.  
4. Check **Initialize this repository with a README**.  
5. Click **Create Repository**.  

---

###  Step 2: Add Your Website Files

1. Upload your website files — `index.html`, `style.css`, `script.js`, etc.  
2. Commit your changes.  
3. You can do this via:
   - GitHub web upload  
   - GitHub Desktop  
   - Visual Studio Code  

---

###  Step 3: Enable GitHub Pages

1. Go to **Settings → Pages**.  
2. Under **Source**, select:
   - **Branch:** `main`
   - **Folder:** `/ (root)` or `/docs`
3. Click **Save**.  
4. GitHub will generate a URL like:
   
---

###  Step 4: Add a Custom Domain

1. In **Settings → Pages**, under **Custom Domain**, type your domain:
2. 2. Click **Save**.  
3. GitHub will automatically create a `CNAME` file with your domain name.

---

###  Step 5: Configure Cloudflare DNS

1. Log in to your [Cloudflare Dashboard](https://dash.cloudflare.com).  
2. Choose your domain → go to the **DNS** tab.  
3. Add these records:

#### 🔸 Root Domain (`example.com`)
| Type | Name | Value | Proxy |  
|------|------|--------|-------|  
| A | @ | 185.199.108.153 | ☁️ Proxied |  
| A | @ | 185.199.109.153 | ☁️ Proxied |  
| A | @ | 185.199.110.153 | ☁️ Proxied |  
| A | @ | 185.199.111.153 | ☁️ Proxied |  

#### 🔸 Subdomain (`www.example.com`)
| Type | Name | Value | Proxy |  
|------|------|--------|-------|  
| CNAME | www | yourusername.github.io | ☁️ Proxied |  

4. Save all changes.

---

###  Step 6: Enable SSL/TLS in Cloudflare

1. Go to **SSL/TLS** in your Cloudflare Dashboard.  
2. Set **Encryption Mode** → `Full`.  
3. Wait a few minutes for Cloudflare to issue the SSL certificate.  

 Your site will now automatically use HTTPS.

---

###  Step 7: Test Everything

1. Open your browser and visit your domain:  

2. If DNS propagation is complete, your website should load successfully.  
3. Wait up to **24 hours** if changes are still updating.  

---

###  Step 8: Watch the Tutorial Video

 Watch the reference video (if available) to better understand each step visually.

---

##  Tips & Optional Enhancements

-  Use **Cloudflare Page Rules** to redirect:
- `www → non-www` (or vice versa)
- `http → https`  
-  Enable **Auto Minify** and **Brotli Compression** under **Speed → Optimization** in Cloudflare.  
-  Commit often to keep your GitHub Pages updated automatically.  

---

##  Final Result

You now have a fully working setup:
-  Free static site hosted on **GitHub Pages**  
-  Secured and accelerated by **Cloudflare**  
-  Protected by SSL/HTTPS  
-  Managed easily via your **GitHub repository**

---

### Need Help?

If something doesn’t work:
- Recheck your DNS settings on Cloudflare  
- Verify your GitHub Pages URL  
- Wait for DNS propagation (~30 mins to 24 hrs)  
- Or refer to Cloudflare + GitHub Pages documentation or contact me

---

✨ **Enjoy your free, secure, and fast website!**

