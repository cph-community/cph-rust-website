# Copenhagen Rust Community website

Static site built with Zola.

## Updating an event

The `events.toml` file stores all the events. Edit the file in a pull request (using the GitHub web editor is fine). Once merged, the site will automatically deploy a new version.

## Local development

1. Clone the repository.

1. [Install](https://www.getzola.org/documentation/getting-started/installation/) Zola.

1. Run the site in preview mode:

    zola serve

Note: The `events.toml` file is only loaded on startup and changes to it will not trigger live reload.