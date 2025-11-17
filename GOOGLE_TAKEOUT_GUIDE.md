# Google Takeout - Download Your Google Data

## Step-by-Step Instructions:

### 1. Start the Export
Go to: **https://takeout.google.com/**

### 2. Select Data to Export
- Click **"Deselect all"** at the top
- Check the services you want to backup (e.g., **"Google Photos"**, **"Drive"**, etc.)
- Click **"Next step"** at the bottom

### 3. Configure Export Settings
- **Delivery method**: "Send download link via email"
- **Frequency**: "Export once"
- **File type**: ".zip"
- **File size**: "50 GB" (recommended, or choose smaller if you prefer multiple files)

### 4. Create Export
- Click **"Create export"**
- Google will process your request

### 5. Wait for Email
- You'll receive an email at: **dominick.do.campbell@gmail.com**
- Processing usually takes a few hours (could be up to 24 hours for large libraries)
- The email will have download links

### 6. Download the Files
Once you receive the email:
- Click the download links in the email
- Save the .zip file(s) to this directory: `takeout/`

### 7. Extract the Photos
After downloading, run:
```bash
cd takeout/
unzip takeout-*.zip
```

### 8. Commit to GitHub (Optional)
```bash
cd ..
./auto_commit.sh
git push
```

---

**Note**: Google Takeout includes all data at full quality with metadata (EXIF data, captions, etc.)
- Downloads are available for 7 days after creation
- You can create a new export anytime
