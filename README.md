# How to Upload a Document or PDF to GitHub

**A2V Internal Guide | April 2026**

---

## Before You Start

Make sure you have the following before uploading:

- A GitHub account (if you don't have one, go to [github.com](https://github.com) and click **Sign up**)
- Access to the A2V repository — ask your A2V administrator if you are unsure
- The PDF or document file ready on your computer

> 💡 Bookmark the repository once you have access: https://github.com/a2vdev/a2vdev.github.io

---

## Step 1 — Go to the A2V Repository

1. Open your web browser and go to [github.com](https://github.com)
2. Sign in to your GitHub account
3. Go directly to the A2V repository: https://github.com/a2vdev/a2vdev.github.io
4. Click the repository name to open it

---

## Step 2 — Navigate to the Correct Folder

Documents must be placed in the correct folder so QR codes can find them. The folder structure is:

```
guide/
  └── 0000/          ← project number folder
        └── your-file.pdf
```

1. Click on the `guide` folder
2. Click on the folder that matches your project number (e.g. `0000`)
3. If the folder does not exist yet, see [Creating a New Project Folder](#creating-a-new-project-folder) at the end of this guide

---

## Step 3 — Name Your File Correctly

File names must be **lowercase**, with **hyphens instead of spaces**, and end in `.pdf`. This keeps links consistent and avoids broken QR codes.

| ✅ Good file name | ❌ Avoid |
|---|---|
| `crossstitch-blue.pdf` | `Cross Stitch Blue.pdf` |
| `xt400-instructions-v2.pdf` | `XT400 Instructions (FINAL).pdf` |
| `product-manual-en.pdf` | `scan0023.pdf` |

> 💡 If updating an existing file, add a version number (e.g. `crossstitch-blue-v2.pdf`) rather than overwriting the original. This prevents broken links for QR codes already in the field.

---

## Step 4 — Upload Your File

1. Inside the correct project folder, click the **"Add file"** button near the top right of the file list
2. Click **"Upload files"** from the dropdown
3. On the upload page, either drag and drop your PDF onto the dotted area, or click **"choose your files"** to browse your computer
4. Wait for the upload to finish — you will see a tick when it is done

---

## Step 5 — Save the Upload (Commit)

Once your file is uploaded you need to save it to the repository. GitHub calls this a **"commit."**

1. Scroll down to the **"Commit changes"** section
2. In the first text box, type a short description of what you are adding, for example:
   - `Add instructions for cross-stitch blue`
   - `Upload XT400 manual v2`
3. Leave the option set to **"Commit directly to the main branch"**
4. Click the green **"Commit changes"** button

> 💡 Your file is now live in the repository and accessible via the docs.a2v.com URL.

---

## Step 6 — Get the File URL

Once uploaded, your file is available at a predictable URL. You do not need to copy anything from GitHub — just build the URL using this format:

```
https://docs.a2v.com/guide/<Project Number>/<File Name>
```

> **Important:** Do not include `.pdf` at the end of the URL. Cloudflare routing automatically handles the file extension — the URL without `.pdf` is what goes into the QR code and the redirect system.

For example, if your project number is `0000` and your file is `crossstitch-blue.pdf`, the QR code URL is:

```
https://docs.a2v.com/guide/0000/crossstitch-blue
```

> 💡 Notice there is no `.pdf` at the end — Cloudflare adds this automatically behind the scenes.

**To confirm the URL is working:** open the URL in your browser. If the PDF loads, it is ready. If you see a 404 error, double-check the project number and file name for typos.

Share this URL with your A2V administrator so they can update the QR redirect to point to the new file.

---

## Step 7 — Test the QR Code

1. Find the QR code for the product
2. Scan it with your phone
3. Confirm it opens the correct document

If it does not work, check:

- The file is in the correct folder
- The file name matches exactly (including capitalisation and hyphens)
- The administrator has updated the redirect to point to the new file

---

## ⚠️ WARNING — Deleting Files from GitHub

> **Think Before You Delete — Read This Carefully**
>
> Deleting files from GitHub is not as simple as it looks and can cause serious, hard-to-fix problems:
>
> - Git keeps a permanent history — deleted files require extra technical steps to fully remove and may still be accessible to others with repository access.
> - Any QR code pointing to a deleted file will **immediately stop working** for every product already in the field.
> - Recovering a mistakenly deleted file requires administrator intervention and can take significant time.
>
> **Before deleting ANY file, please double-check and triple-check that:**
>
> - No QR code currently points to that file
> - Your A2V administrator has confirmed it is safe to remove
> - A replacement file (if needed) is already uploaded and working
>
> **If in doubt — do NOT delete. Contact your A2V administrator first.**

---

## Creating a New Project Folder

If you are adding instructions for a brand new product and the project folder does not exist yet:

1. Navigate to the `guide/` folder in the repository
2. Click **"Add file"** then **"Create new file"**
3. In the file name box, type the project number followed by `/` and a placeholder name:
   ```
   1234/.gitkeep
   ```
   *(This creates the folder `1234/` with an empty placeholder file that GitHub needs to store an empty folder.)*
4. Scroll down and click **"Commit changes"**
5. Go back into the new folder and follow Steps 3–5 above to upload your PDF

> ⚠️ Always let your A2V administrator know when you create a new project folder so they can add the QR redirect for that product.

---

## Updating an Existing Document

1. Upload the new file with an updated name (e.g. add `-v2` or the date: `crossstitch-blue-v2.pdf`)
2. Note the new URL using the format from [Step 6](#step-6--get-the-file-url) (without `.pdf` at the end)
3. Let your A2V administrator know the new URL so they can update the redirect
4. **Do not delete the old file** — someone in the field may still have the old QR code

---

## Getting Help

| Problem | Solution |
|---|---|
| Can't find the repository | Ask your A2V administrator for the direct link: https://github.com/a2vdev/a2vdev.github.io |
| Don't have permission to upload | Ask your A2V administrator to add you as a contributor |
| File uploaded but QR code not working | The redirect may need updating — send your administrator the URL from Step 6 |
| Not sure if the URL is correct | Check the URL in your browser first to confirm the file is accessible |

---

*A2V Internal Guide | April 2026 | [docs.a2v.com](https://docs.a2v.com)*
