An investigation into the arms trade, with a specific focus around Greater Manchester

The real content is within the `content` directory, which is what gets published to the webpage

## Contributing

We encourage PRs to add/edit content. When creating new pages they:

- Must include a title in the frontmatter
- Must be within the `content` directory and not in any sub-directory
- Should link to/from any existing pages to make them easier to discover
- Should include any relevant tags in the frontmatter

The easiest way of achieving this is by copying an existing file and following the same format.

The use of [Obsidian](https://obsidian.md/) makes working with the content easier, but you can use any editor you like as long as it can cope with Markdown files.

PRs should be to the `hugo` branch

## Development

This project is bulit on top of [Quartz](https://github.com/jackyzha0/quartz) and uses [Obsidian](https://obsidian.md/), [Hugo](https://gohugo.io/), and [Hugo-Obsidian](https://github.com/jackyzha0/hugo-obsidian). You will need all three of these installed for a full development environment.

Ordinarily GitHub Actions will perform the Obsidian to Hugo conversion and static site build whenever code is merged into the `main` branch. But for local development you can run the following:

1. `hugo-obsidian -input=content -output=assets/indices -index -root=.` to generate the backlinks
2. `hugo serve` to serve the website locally
3. `open http://localhost:1313` or click on http://localhost:1313 to open the website in your web browser

PRs should be to the `hugo` branch. GitHub Actions pushes the generated HTML to the `main` branch, which will be overwritten every time new content is pushed.
