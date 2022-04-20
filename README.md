# _pandoc-artifact_

[![Pandoc CI](https://github.com/gmarmstrong/pandoc-artifact/actions/workflows/main.yml/badge.svg)](https://github.com/gmarmstrong/pandoc-artifact/actions/workflows/main.yml)
[![GitHub](https://img.shields.io/github/license/gmarmstrong/pandoc-actions?color=informational)](LICENSE)

This project demonstrates a GitHub Actions workflow for using [pandoc](https://pandoc.org/) to convert a Markdown file, `docs/SLIDES.md`, into an interactive [reveal.js](https://revealjs.com/) slideshow presentation. The task is automatically run upon any push, pull request, or manual workflow dispatch. The output HTML file is then uploaded to the GitHub repository's build artifacts, which is available for download from ([through the web browser, the GitHub CLI](https://docs.github.com/en/actions/managing-workflow-runs/downloading-workflow-artifacts), [or even another Action](https://github.com/actions/download-artifact)) _without_ having to commit a build artifact to source.

## Demo

<a href="https://github.com/gmarmstrong/pandoc-artifact/actions/runs/2192821405"><img src="https://i.imgur.com/yt2zEJ1.png" alt="Screenshot of a demo build result and the resulting link to the build artifact, SLIDES.html"/></a>
<img src="https://i.imgur.com/OCxousD.gif" alt="Short screen recording of a demo slideshow"/>

## Known limitations

+ Due to [a limitation of GitHub](https://github.com/actions/upload-artifact/issues/51), artifact download URLs only work for registered GitHub users, even if the repository is public. The link will 404 if a user is not logged in.
