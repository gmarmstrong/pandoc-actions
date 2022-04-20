# _pandoc-actions_

This workflow demonstrates a GitHub Action which uses [pandoc](https://pandoc.org/) to convert a simple Pandoc Markdown file, `docs/SLIDES.md`, to an interactive [reveal.js](https://revealjs.com/) slideshow presentation. The output HTML file is then uploaded to the GitHub repository as a build artifact, which is available for [download through the GitHub repository](https://docs.github.com/en/actions/managing-workflow-runs/downloading-workflow-artifacts) (through the web browser, CLI, [or even another Action](https://github.com/actions/download-artifact)) _without_ having to commit the build artifact to source.

## Demo

<a href="https://github.com/gmarmstrong/pandoc-actions/actions/runs/2192821405"><img src="https://i.imgur.com/yt2zEJ1.png" alt="Screenshot of a demo build result and the resulting link to the build artifact, SLIDES.html" height="280"/></a>
<img src="https://i.imgur.com/OCxousD.gif" alt="Short screen recording of a demo slideshow" height="280"/>

## Known limitations

+ Due to [a limitation of GitHub](https://github.com/actions/upload-artifact/issues/51), artifact download URLs only work for registered GitHub users, even if the repository is public. The link will 404 if a user is not logged in.
