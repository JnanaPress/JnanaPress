# JnanaPress

## Dependencies

- brew install qpdf

## Processing

- `qpdf --split-pages book.pdf page-%d.pdf`
- `uv run marker_single --output_format markdown ./page-133.pdf --output_dir .`

```
for i in page*.pdf; do
    uv run marker_single --output_format markdown $i --output_dir .
done
```

```
marker . --output_dir .
```

- Replace <br> with <br/>

# Website

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

### Installation

```
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.
