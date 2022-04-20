# _pandoc-artifact_

[![Pandoc CI](https://github.com/gmarmstrong/pandoc-artifact/actions/workflows/main.yml/badge.svg)](https://github.com/gmarmstrong/pandoc-artifact/actions/workflows/main.yml)
[![GitHub](https://img.shields.io/github/license/gmarmstrong/pandoc-actions?color=informational)](LICENSE)

GitHub Action to run [pandoc](https://pandoc.org/) tasks and create build artifacts from them.

The demo gives an example workflow of converting a simple Pandoc Markdown file, `docs/SLIDES.md`, to an interactive [reveal.js](https://revealjs.com/) slideshow presentation. The output HTML file is then uploaded to the GitHub repository as a build artifact, which is available for [download through the GitHub repository](https://docs.github.com/en/actions/managing-workflow-runs/downloading-workflow-artifacts) (through the web browser, CLI, [or even another Action](https://github.com/actions/download-artifact)) _without_ having to commit the build artifact to source.

## Demo

<a href="https://github.com/gmarmstrong/pandoc-artifact/actions/runs/2192821405"><img src="https://i.imgur.com/yt2zEJ1.png" alt="Screenshot of a demo build result and the resulting link to the build artifact, SLIDES.html"/></a>
<img src="https://i.imgur.com/OCxousD.gif" alt="Short screen recording of a demo slideshow"/>

## Known limitations

+ Due to [a limitation of GitHub](https://github.com/actions/upload-artifact/issues/51), artifact download URLs only work for registered GitHub users, even if the repository is public. The link will 404 if a user is not logged in.
