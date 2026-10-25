NexoraWorld automatic news setup

This update adds an automatically refreshed Live World Headlines section. A GitHub Actions workflow fetches BBC News RSS headlines from World, Technology and Business feeds about every 6 hours, creates news.json, and deploys the site to GitHub Pages. Headlines link readers to the original BBC page; this does not republish full articles.

IMPORTANT SETUP:
1. Upload the updated index.html to the root of https://github.com/musman986/nexoraworld and replace the old file.
2. Create a new file named exactly .github/workflows/update-news.yml and paste the contents from that file in this package. Commit it to main.
3. Open Settings > Pages > Build and deployment > Source, select GitHub Actions. Save if needed.
4. Open Actions, choose "Update world news and publish site", and click Run workflow once. Wait for the run to finish green.
5. The schedule runs every 6 hours; scheduled workflow timing may be delayed by GitHub. You can also manually run it from Actions.

The GitHub repository is public, so its contents and the website are public. Do not add passwords, API keys, or private information. Check BBC feed terms before changing how content is used. The workflow displays short feed descriptions and links to the publisher, not full story text. News availability depends on the source feed and GitHub Actions.
