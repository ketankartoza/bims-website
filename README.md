# BIMS Website

Handbook and Technical Docs Repository for the Biodiversity Information Management System (BIMS). Here is where we highlight the procedures, principles, and processes related to using, managing and developing the BIMS platform. Please review this content at [https://kartoza.github.io/bims-website](https://kartoza.github.io/bims-website) for more information.

## Building the Handbook as a PDF

### Check out the code

```bash
git clone git@github.com:kartoza/bims-website.git
```

### Install Dependencies

You need to install these packages:

```bash
pip install mkdocs-with-pdf
pip install mkdocs-material
pip install mdx_gh_links
pip install mkdocs-pdf-export-plugin
```

### Build the documentation

> Note that whenever you add new sections to nav in the mkdocs.yml
> (used for building the web version), you should apply those same
> edits to mkdocs-base.yml if you want those new sections to appear
> in the pdf too.

```bash
cd docs
./build-docs-pdf.sh
xdg-open TheBIMSHandbook.pdf
```
