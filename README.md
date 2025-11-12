# Cloud Backup from Google Drive

This repository backs up files from Google Drive to GitHub.

## Setup

1. **Install rclone** (if not already installed):
   ```bash
   curl https://rclone.org/install.sh | sudo bash
   ```

2. **Configure rclone for Google Drive**:
   ```bash
   rclone config
   ```
   - Choose `n` for new remote
   - Name it `gdrive`
   - Choose `Google Drive` from the list
   - Follow prompts to authenticate with: **dominick.do.campbell@gmail.com**
   - Accept default settings for most options

## Usage

### Sync files from Google Drive:
```bash
./sync_from_gdrive.sh
```

This will download all files from your Google Drive to the `gdrive_backup/` directory.

### Commit and push to GitHub:
```bash
./auto_commit.sh
git push
```

Or manually:
```bash
git add gdrive_backup/
git commit -m "Backup from Google Drive"
git push
```

## Files

- `sync_from_gdrive.sh` - Downloads files from Google Drive using rclone
- `auto_commit.sh` - Automatically commits changes to git
- `gdrive_backup/` - Directory containing synced files (created on first sync)

## Notes

- The sync uses `rclone sync` which mirrors Google Drive to local
- Excluded files: .DS_Store, *.tmp, Thumbs.db, desktop.ini
- Large files may take time to download
