This is the repo containing the source content for the [CDPS code club site](https://cdpscc.github.io). 

The site is built using the [Hugo](https://gohugo.io/) static site generator. Hugo was chosen because it is a self contained single executable file - no language specific runtime environments and library dependencies to worry about. Being fast and having lots of nice features was an added bonus.

There are two git submodules in this repo:
* `cdpscc/themes/bootie-docs` a customised fork of the [bootie-docs](https://github.com/key-amb/hugo-theme-bootie-docs) Hugo theme.
* `cdpscc/public` the Hugo site build directory which overlaps the github pages organisation repo hosting the site itself. For github pages we used an organisation repo instead of a project repo so we could put content at the root level. This means it needed a separate repo.

## Cloning repo

To clone this repo, it is recommended to use the `--recursive` option to clone the submodules at the same time.

eg:
```
$ git clone --recursive ...
```

## Installing Hugo

## Editing content

The content is in markdown text files for easy editing.

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

## Building site

## Testing

To start a local web server for testing the site, run (from the cdpscc subdirectory):
```
$ hugo server
```
Then point your browser at http://localhost:1313 to browse the site.

This local web server will detect changes to most files and automatically rebuild/reload them on the fly (nice)

## Deploying
