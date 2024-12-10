# Wanderer

The Wanderer is a framework for telling non-linear and interactive stories with videos and linked data. It's designed for exhibitions and the web. 

![Screenshot of the Xingu Entangled Wanderer](wanderer.png)

## Examples

- [Demo](https://uclab-potsdam.github.io/wanderer-demo)
- [Xingu Entangled](https://uclab-potsdam.github.io/xingu-entangled)
- [this empty Wanderer instance](https://uclab-potsdam.github.io/wanderer)

## Creating your own Wanderer instance

The Wanderer is a static web page and does not depend on a dedicated database or any other backend infrastructure. To create your own Wanderer instance simply copy/download/fork this repository and put the files on a web server.

The files in this branch are prebuild. If you want to contribute to or customise the Wanderer [checkout `main`](https://github.com/uclab-potsdam/wanderer/tree/main).

## Authoring

You can make changes to any wanderer instance by appending `/#/authoring` to its url (e.g. [https://uclab-potsdam.github.io/wanderer-demo/#/authoring](https://uclab-potsdam.github.io/wanderer-demo/#/authoring) or [https://uclab-potsdam.github.io/wanderer/#/authoring](https://uclab-potsdam.github.io/wanderer/#/authoring)). All edits are local and saved inside your web browser. Making changes public to everyone requires exporting the data and replacing the database file `db.json`.

## Hosting

To host the wanderer put the files in this repository, your customised `db.json` and any media files on a web server.

### GitHub

You can host the wanderer directly through [GitHub pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site). But there are [limits on file sizes](https://docs.github.com/en/repositories/working-with-files/managing-large-files/about-large-files-on-github) which are easily exceeded when using video files.

You can host your media files on another web server. Make sure to enable [Cross-Origin Resource Sharing (CORS)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS).

Alternatively you can create small proxy video files with lower resolution and reduced quality and replace them with the origial files once you're ready to move to another server.

### Local

You can [create a local webserver](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Tools_and_setup/set_up_a_local_testing_server) to run the wanderer on your computer.

## Directory Structure

- `/assets/` this folder contains the necessary scripts, stylesheets, etc. to run the Wanderer. Best not to change anything here. Those files are minified and barely readable, checkout the `main` branch containing the source files if you want to change how the wanderer functions and looks.
- `/files/` this is the default folder for all media files such as videos, images, subtitles, the about text and the favicon. You can change the name of this directory if you update the config section in the `db.json` file accordingly.
- `/files/about.md` this is the default file for the content of the about text accessible thorugh the ℹ icon in the interface. It's a [Markdown file](https://www.markdownguide.org/getting-started/) and can be edited in any text editor or directly on GitHub. You can specify the file name in the config section of the `db.json` file and specifiy localized about files (e.g. about_de.md) to support multiple languages.


## The Database File

## Updating the Wanderer
