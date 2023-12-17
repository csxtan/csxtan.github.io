# Website management


## How to publish

To start preview: `yarn dev`

To publish to GitHub Pages (csxtan.github.io):
    Push to GitHub and the rest will be done automatically by a GitHub action.

- site generation is not necessary
- [publication status](https://github.com/csxtan/csxtan.github.io/actions)

To publish to UChicago (math.uchicago.edu/~cindy):
    Generate site: `yarn build`
    Connect to UChicago VPN via Cisco AnyConnect.
    Transfer files:
        `scp -r dist/* cindy@math.uchicago.edu::~/public_html`
        (password is in Bitwarden)
    (If new files have been added) SSH into server and update file permissions:
        `ssh cindy@math.uchicago.edu`
        `chmod og+rx -R ~/public_html/`

    - [more information on math department publishing](https://math.uchicago.edu/miscellany/making-a-website/current-website-guide.pdf)

## File organization

src/pages/: pages (markdown) and layouts
- index.md (homepage content)
- _index.astro (homepage layout)
- _page.astro (layout for a simple markdown page with a link to return to homepage)

src/styles/: stylesheets

public/: images and files

- [astro directory structure](https://docs.astro.build/en/core-concepts/project-structure/)

## Design notes

- all the triangles are done in CSS ::before and ::after
- responsive design using [utopia clamps](https://utopia.fyi/clamp/calculator/)
- ! the 404 file doesn't work!
