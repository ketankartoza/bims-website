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
### How to edit the documentation online

Go to the folders with the content:

https://github.com/kartoza/bims-website/tree/main/docs/src


Click on any of the files with .md extension then click the pencil to edit:

![image](https://user-images.githubusercontent.com/178003/195879617-2bc4e14e-0d16-432a-a260-8e3de42013da.png)


Editing the content uses exactly the same system as editing a ticket so you should hopefully feel at home there if you already have worked with GitHub issues. You can use the preview option to see how your changes look:

![image](https://user-images.githubusercontent.com/178003/195879644-3238b4f4-ec38-4e00-935a-dc803da4fb1c.png)


Once you are done editing, scroll down the page and write a short message explaining your changes (1) then choose commit directly to the main branch (2) then commit (3) 

![image](https://user-images.githubusercontent.com/178003/195879687-9234d6bd-9d05-43d6-9e90-cff10c655278.png)


Normally we would actually ask you to make a branch and a pull request, but use option (2) for now to keep things simple.
Your changes should appear on the live site within a minute or so.
