# Eclipse Che UI Customization

This document describes the process for customizing the **Eclipse Che UI**, including logos, text, and favicon.

---

## 🔧 Customization Process

### 1. Edit UI Metadata

Edit the file:

`01-che-dashboard-branding-meta/product.json`

Use the following reference for guidance:  
[Reference – branding.constant.ts (GitHub)](https://github.com/eclipse-che/che-dashboard/blob/main/packages/dashboard-frontend/src/services/bootstrap/branding.constant.ts)

---

### 2. Add Your Favicon

Place your custom `favicon.ico` file in the folder:

`02-che-branding-favicon/`

> **Important notes:**
> 1. You may rename your file, but **do not change the Secret key**.
> 2. The file **must be in `.ico` format**.
> 3. Default name: `favicon.ico`.

> The `kustomization.yaml` file will automatically handle base64 encoding.

---

### 3. Add Loader Image

Add your custom **loading image** inside:

`03-che-dashboard-loader-image/`

> **Notes:**
> 1. You may rename the file, but **keep the same Secret key**.
> 2. The file **must be in `.svg` format**.
> 3. Default name: `loader.svg`.

---

### 4. Add Main Logo

Place your **main logo image** (displayed after login on the main page) inside:

`04-che-dashboard-branding-logo/`

> **Notes:**
> 1. You may rename your file, but **do not modify the Secret key**.
> 2. The file **must be in `.svg` format**.
> 3. Default name: `che-logo.svg`.

---

## 🚀 Apply Customization

Once all assets are in place, apply the root `kustomization.yaml`:

`kubectl apply -k .`

---

## 💡 Recommendations

- For both `loader.svg` and `che-logo.svg`, download the **original images** first and **resize them to match the originals** to avoid rendering or scaling issues.

---

**End of document.**

