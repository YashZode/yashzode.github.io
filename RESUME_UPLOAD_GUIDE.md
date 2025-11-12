# Resume Upload Guide

## 📄 Where to Upload Your Resume

### **Location: Root Directory**

Upload your resume PDF file to the **root directory** of your repository (same folder as `index.html`).

### **File Name**

Name your resume file exactly: **`YashZode_Resume.pdf`**

This matches the download link in the portfolio (line 134 of `index.html`).

## 📁 Current File Structure

```
yashzode.github.io/
├── index.html
├── styles.css
├── script.js
├── README.md
├── YashZode_Resume.pdf  ← Upload your resume here
├── assets/
│   ├── images/
│   └── icons/
└── ...
```

## ✅ Steps to Upload

### Option 1: Using GitHub Web Interface

1. Go to your repository: https://github.com/YashZode/yashzode.github.io
2. Click **"Add file"** → **"Upload files"**
3. Drag and drop your resume PDF or click to browse
4. **Important:** Rename the file to `YashZode_Resume.pdf` if it has a different name
5. Scroll down and click **"Commit changes"**
6. Your resume will be available at: `https://yashzode.github.io/YashZode_Resume.pdf`

### Option 2: Using Git Command Line

```bash
# Navigate to your repository
cd path/to/yashzode.github.io

# Copy your resume to the root directory
# Make sure it's named YashZode_Resume.pdf

# Add and commit
git add YashZode_Resume.pdf
git commit -m "Add resume PDF"
git push origin main
```

### Option 3: Using GitHub Desktop

1. Open GitHub Desktop
2. Navigate to your repository
3. Copy your resume PDF to the repository folder
4. Rename it to `YashZode_Resume.pdf`
5. Commit and push the changes

## 🔗 How It Works

The portfolio has a download button in the About section that links to:
```html
<a href="YashZode_Resume.pdf" class="btn btn-primary" download>Download Resume (PDF)</a>
```

When visitors click this button, they will download your resume PDF directly.

## 📝 Alternative Locations (Optional)

If you prefer to organize files differently, you can:

1. **Put it in assets folder:**
   - Upload to `assets/YashZode_Resume.pdf`
   - Update `index.html` line 134 to: `href="assets/YashZode_Resume.pdf"`

2. **Use a different filename:**
   - If your file has a different name, update line 134 in `index.html` to match your filename

## ✅ Verification

After uploading, verify it works by:

1. Visiting: `https://yashzode.github.io/YashZode_Resume.pdf`
2. The file should download or display in your browser
3. Click the "Download Resume" button on your portfolio to test

## 🎯 Current Resume Files in Repository

I noticed you already have several resume PDFs in your repository:
- `YashZode_Resume.pdf`
- `YashZode_Resume.pdf_jan_2025`
- And several others

**Recommendation:** Use `YashZode_Resume.pdf` as your main resume file, or update the link in `index.html` to point to your preferred file (e.g., `YashZode_Resume.pdf_jan_2025`).

---

**Need Help?** If you have any issues uploading or linking your resume, feel free to ask!

