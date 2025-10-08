# Commentathor Blog

This is the repository for my personal blog "Comment-a-Thor" by @schwesig.

## About

A personal blog featuring quotes, thoughts, and musings in German and English.

## Technical Details

- **Static Site Generator**: [Hugo](https://gohugo.io/)
- **Theme**: [Binario](https://github.com/Vimux/Binario)
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

```bash
hugo new posts/post-name.md
```

Edit the generated file in `content/posts/` and set `draft = false` when ready to publish.

## Building for Production

```bash
hugo --minify
```

The generated site will be in the `public/` directory.

## License

Content: © 2025 @schwesig. All rights reserved.

Theme: [Binario](https://github.com/Vimux/Binario) - MIT License
