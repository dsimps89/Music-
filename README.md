# GitHub Pages Music Listening Room with Owner Editor

## Files
- `index.html` — public music website
- `admin.html` — owner editor (GitHub authentication required to save)
- `songs.json` — song titles, artists, albums, years, genres, credits, audio and cover paths
- `site.json` — website title, artist, intro, contact email and legal notice
- `songs/` and `covers/` — media files

## Publish
1. Upload the **contents** of this folder into a GitHub repository's root.
2. In repository Settings → Pages, select Deploy from a branch → main → /(root).
3. Visit your GitHub Pages URL. Public page is `index.html`; owner editor is `admin.html`.

## Owner editing: refresh, upload and save
1. Sign into GitHub and create a **fine-grained personal access token** scoped ONLY to your music repository, with **Contents: Read and write**. GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens. Never commit or share this token.
2. Open `admin.html` on your published website. Enter GitHub username, repository name, branch and the token.
3. Click **Refresh from GitHub** to load the latest data. Edit the website and each song's information.
4. For each song, choose an MP3 or image and click its **Upload** button. Uploading commits the media file immediately. Then click **Save all information to GitHub** to link the media and save edits.
5. Click **Refresh published website** to view your changes. GitHub Pages can take a few minutes to deploy.
6. To revoke access, revoke the token in GitHub. The editor does not store the token after a page reload or tab close.

## Security and limitations
- The public can **view** `admin.html`, but only someone with valid GitHub repository write credentials can **save**. The site cannot verify personal identity independently, and anyone with repository write permission can edit it.
- Token is held only in browser memory, not localStorage or the repository. Use this editor only on your trusted GitHub Pages domain, over HTTPS, on a trusted device. Never share the token. For stronger protection, use a private authenticated backend.
- The upload form limits media files to 20 MB. For larger MP3s, upload using GitHub's repository interface or Git; then paste the file path into the song entry and save. GitHub Pages and GitHub repository limits still apply.
- GitHub Pages is **public hosting**. Hiding download buttons does not prevent listeners from saving audio via browser developer tools or direct file URLs. It is NOT a secure private review portal.
- Copyright disclaimers do not provide legal permission. Do not publish disputed recordings before the necessary rights are cleared. For private industry review, use a secure access-controlled service instead.
