In this technical part of the workshop you:
- Set up your local environment to build a documentation portal
- Understand and configure your own distributed source publishing flow
- Write simple markdown document with additional metadata
- Publish the portal to GitHub Pages

The following technologies are used:
- [Git](https://git-scm.com/) and [GitHub](https://github.com) and [GitHub Pages](https://pages.github.com/)
- [DocPad](https://docpad.org/) and documentation portal template based on it: [docpad-skeleton-apidoc](https://github.com/YaaS/docpad-skeleton-apidocs)
- [Chewie](https://github.com/YaaS/chewie), distributed source publishing tool

### Git

Source control management system for any kind of text files. Allows to keep many versions of one file and merge those into one at any time. 
Set of files can be grouped in so called repositories.

Most known tools:
- Git CLI
- GitHub Desktop
- SourceTree

### GitHub

Git hosting service + much more like:
- Projects management
- Issues reporting
- Wiki

Most known alternative: [Bitbucket](https://bitbucket.org)

### [GitHub Pages](https://pages.github.com/)

Free static pages hosting service. 
Sample lib that hosts its documentation page using GitHub Pages: http://getbootstrap.com/

Most known alternative: I don't know anything better

### DocPad

Static site generator + much more. By defining layouts you can generate whole documentation portals with sources written in simple markdown syntax.

Most known alternatives:
- [Jekyll](https://jekyllrb.com/) and template from [Tom Johnson](https://github.com/tomjohnson1492/documentation-theme-jekyll),
- [Sphinx](http://www.sphinx-doc.org) that is probably behind the [Write the Docs](http://www.writethedocs.org/guide/) community.

### Markdown

Simple markup language used in plain text files. Later such file can be converted into any other format like HTML for example. Sample usage: this document and basically all other documents that describe this workshop.

Most known alternatives:
- [reStructuredText](http://docutils.sourceforge.net/rst.html)
- [AsciiDoc](http://www.methods.co.nz/asciidoc/)

### Chewie

Chewie makes it possible to have documentation content distributed in different locations. It supports content registry management, independent docu generation and publishing.
