# Commentathor Blog

This is the repository for my personal blog "Comment-a-Thor" by @schwesig.

## About

A personal blog featuring quotes, thoughts, and musings in German and English.

**Important Notice:** This website (commentathor.de) is completely independent and has no affiliation whatsoever with commentathor.com. There is no connection in terms of content, politics, or personnel between this blog and any other website using a similar name.

## Technical Details

- **Static Site Generator**: [Hugo](https://gohugo.io/)
- **Theme**: [Cactus](https://github.com/monkeyWzr/hugo-theme-cactus)
- **Language**: German (de)

## Local Development

To run the blog locally:

```bash
# Clone the repository with submodules
git clone --recurse-submodules https://github.com/schwesig/commentathor_de.git
cd commentathor_de

# Start the Hugo development server
hugo server -D

# Visit http://localhost:1313 in your browser
```

## Creating New Posts

### Via Pull Request (Recommended)

1. **Create an Issue** using the "Neuer Blog Post" template
2. **Create a new branch**: `git checkout -b post/post-title`
3. **Create the post**:
   ```bash
   hugo new posts/post-name.md
   ```
4. **Edit the file** in `content/posts/` with your content:
   - Add German quote
   - Add English translation
   - Set author and year
   - Add appropriate tags and categories
   - Set `draft = false` when ready
5. **Test locally**: `hugo server -D`
6. **Commit and push**:
   ```bash
   git add content/posts/post-name.md
   git commit -m "Add new post: Post Title"
   git push origin post/post-title
   ```
7. **Create Pull Request** on GitHub
8. **Merge PR** → Automatic deployment to FTP!

### Direct to Main (Quick Method)

1. Create new post with `draft = true` in frontmatter
2. Commit and push to `main` branch
3. Edit and preview locally with `hugo server -D`
4. When ready to publish: Set `draft = false`
5. Commit and push → **Automatic deployment to FTP via GitHub Actions**

The workflow only deploys when content changes are pushed to `main`.

## Deployment

The blog automatically deploys to FTP when changes are pushed to the `main` branch.

### Required GitHub Secrets:

Set these in your GitHub repository settings (Settings → Secrets and variables → Actions):

- `FTP_SERVER` - FTP server hostname
- `FTP_USERNAME` - FTP username
- `FTP_PASSWORD` - FTP password
- `FTP_DIR` - Remote directory path (e.g., `/public_html/` or `/htdocs/`)

### Manual Build

```bash
hugo --minify
```

The generated site will be in the `public/` directory.

## License

Content: © 2025 @schwesig. All rights reserved.

Theme: [Cactus](https://github.com/monkeyWzr/hugo-theme-cactus) - MIT License
