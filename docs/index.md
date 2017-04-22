# Welcome to MkDocs

For full documentation visit [mkdocs.org](http://mkdocs.org).

[TOC]

## Using this template

### Clone the template

```
git clone https://github.com/gpduck/MkDocsSiteTemplate.git NewSiteName
```

### Customize the configuration

Update the following settings in the `mkdocs.yml` file:

| Name | Description |
| ---- | ----------- |
| site_name | The title and Home link for your site |
| repo_url  | The base link to a git repository for your site |
| repo_name | The name to use in the "Edit on" links |
| edit_uri  | The base path for the edit page on the git repo |

The examples included in the template work for GitHub, examples for other sites are on the [mkdocs user guide](http://www.mkdocs.org/user-guide/configuration/).

### Build/Serve content locally

You'll need to have python and pip installed, get them [here](https://www.python.org/downloads/).

Then you'll need to install the python packages:

```
pip install -r requirements.txt
```

Now you should be able to run mkdocs:

| Command | Purpose |
| ------- | ------- |
| mkdocs build | Generates site content in `./site` |
| mkdocs serve | Generates site content in `./site` and starts a built-in webserver on [http://localhost:8000](http://localhost:8000) |

### Build pipelines

The site template includes configuration files for [AppVeyor](https://appveyor.com) and [Jenkins](https://jenkins.io) that should be imported automatically
if you configure a project pointed at your Git repo.  There is also a PowerShell script `.\build.ps1` that will install the pip packages, run build, and package
the site contents in a *.nupkg file (for deploying via [OctopusDeploy](https://octopus.com))


## Syntax

In the template, MkDocs is configured to use [Python Markdown](https://pythonhosted.org/Markdown/).  A synax reference
can be found [Here](http://daringfireball.net/projects/markdown/syntax).

The following [Python Markdown extensions](https://pythonhosted.org/Markdown/extensions/index.html) are enabled
by default in this project template:

* [pymdownx.superfences](http://facelessuser.github.io/pymdown-extensions/extensions/superfences/)
* [Meta-Data](https://pythonhosted.org/Markdown/extensions/meta_data.html)
* [Table of Contentx](https://pythonhosted.org/Markdown/extensions/toc.html)
* [CodeHilite](https://pythonhosted.org/Markdown/extensions/code_hilite.html):
* [Admonition](https://pythonhosted.org/Markdown/extensions/admonition.html)

The default code hilighting has been replaced with [Pygments](http://pygments.org/docs/) via the CodeHilite plugin.
Some style tweaks have been added to `docs/theme_dir/css/codehilite.css`.  Language detection has been disabled, so
code blocks need to have their language specified using the [Pygments Language Name](http://pygments.org/languages/) like this:

\`\`\`PowerShell  
  code here  
\`\`\`

## MkDocs Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml          # The configuration file.
    docs/
        index.md        # The documentation homepage.
        ...             # Other markdown pages, images and other files.
    docs/theme_dir/css
        custom.css      # Css customizations
