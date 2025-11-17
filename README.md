# Google Takeout Backup

This repository stores backups from Google Takeout (Google Photos, Google Drive, etc.) on GitHub.

## Usage

### Download from Google Takeout:

See detailed instructions in: **[GOOGLE_TAKEOUT_GUIDE.md](GOOGLE_TAKEOUT_GUIDE.md)**

Quick summary:
1. Go to: https://takeout.google.com/
2. Select the data you want to export (Google Photos, Google Drive, etc.)
3. Choose export settings (50 GB zip files recommended)
4. Wait for email with download links (usually a few hours)
5. Download and extract to `takeout/` directory

### Commit and push to GitHub:
```bash
./auto_commit.sh
git push
```

Or manually:
```bash
git add takeout/
git commit -m "Backup from Google Takeout"
git push
```

## Files

- `auto_commit.sh` - Automatically commits changes to git
- `takeout/` - Directory for Google Takeout downloads
- `GOOGLE_TAKEOUT_GUIDE.md` - Step-by-step guide for downloading from Google Takeout

## Notes

- Google Takeout includes all your data at full quality with metadata
- Large exports may take hours to process
- Downloads are available for 7 days after creation
