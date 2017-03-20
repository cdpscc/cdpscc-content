This is the repo containing the source content for the [CDPS code club site](https://cdpscc.github.io). 

The site is built using the [Hugo](https://gohugo.io/) static site generator. Hugo was chosen because it is a self contained single executable file - no language specific runtime environments and library dependencies to worry about. Being fast and having lots of nice features was an added bonus.

There are two git submodules in this repo:
* `cdpscc/themes/bootie-docs` a customised fork of the [bootie-docs](https://github.com/key-amb/hugo-theme-bootie-docs) Hugo theme.
* `cdpscc/public` the Hugo site build directory which overlaps the github pages organisation repo hosting the site itself. For github pages we used an organisation repo instead of a project repo so we could put content at the root level. This means it needed a separate repo.

## Cloning repo

To clone this repo, it is recommended to use the `--recursive` option to clone the submodules at the same time.

eg:
```
$ git clone --recursive git@github.com:cdpscc/cdpscc-content.git
```

Otherwise you'd need to init each submodule separately to get their code.

## Installing Hugo

Download the latest Hugo release for your platform [here](https://github.com/spf13/hugo/releases) and put it somewhere on your PATH.

And there is also a [quickstart guide](https://gohugo.io/overview/quickstart/).

## Editing content

The content is in markdown text files for easy editing. Github publishes a good [markdown reference](https://guides.github.com/features/mastering-markdown/).

There are also client site JS libraries included for code syntax highlighting and rendering of scratch blocks.

eg Python markdown syntax:
```
    ```python
    def myfunc(param):
        print('Hello!')
    ```
```
or [Scratch block rendering](https://wiki.scratch.mit.edu/wiki/Block_Plugin):
```
    ```blocks
    when flag clicked
        say [Hello!]
    ```
```
Look at the markdown source for more examples.

## New pages

_TODO: test these docs a bit more_

A new page can be created with the following example hugo command (in the `cdpscc` directory):
```
$ hugo new python/new_python_doc.md
```
Then edit the metadata (eg title, categories etc) at the top of the new file, and add your markdown content below.

## Building site

To build the output for the site in `cdpscc/public`, run (from the cdpscc subdirectory):
```
$ hugo
```

_TODO: test/document cleaning out of the public directory first_

## Testing

To start a local web server for testing the site, run (from the cdpscc subdirectory):
```
$ hugo server
```
Then point your browser at http://localhost:1313 to browse the site.

This local web server will detect changes to most files and automatically rebuild/reload them on the fly (nice).

## Deploying

Once the output is built in the `cdpscc/public` directory, the changes can be committed and pushed to the cdpscc.github.io repo to go 'live'.

Feel free to create pull requests for content changes if that sounds a bit scary.
