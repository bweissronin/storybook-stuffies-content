# Storybook Stuffies - Dynamic Content

This repository hosts downloadable content for the Storybook Stuffies iOS app.

## Structure

```
├── manifest.json           # Master list of all available characters
└── characters/
    ├── leo/
    │   ├── character.json  # Character metadata and configuration
    │   ├── stories.json    # All stories for Leo
    │   └── assets/         # Character sprites, expressions, environments, storybook pages
    └── daisy/
        ├── character.json
        ├── stories.json
        └── assets/
```

## Updating Content

### Adding a New Character

1. Create directory: `characters/NEW_CHARACTER_NAME/`
2. Add `character.json` with character metadata
3. Add `stories.json` with story content
4. Upload assets to `characters/NEW_CHARACTER_NAME/assets/`
5. Update `manifest.json` to include new character
6. Commit and push - app will auto-detect new content!

### Updating Existing Character

1. Increment version in `character.json` or `stories.json`
2. Update content as needed
3. Update `manifest.json` version and `last_updated` timestamp
4. Commit and push - app will auto-download updates

## Asset Guidelines

- **Sprites**: PNG format, transparent background
- **Story Pages**: JPG format, max 2048px width
- **File Naming**: Use lowercase with hyphens (e.g., `bella-bunny-body.png`)
- **Compression**: Optimize images before uploading

## Version Control

- **manifest.json version**: Increment when adding/removing characters
- **character.json version**: Increment when changing character structure
- **stories.json version**: Increment when adding/updating stories

## GitHub Pages

Content is automatically served via GitHub Pages at:
`https://bweissronin.github.io/storybook-stuffies-content/`

Changes pushed to `main` branch are live within minutes.
