# Libretro Documentation

This is the source for the [libretro documentation](https://buildbot.libretro.com/docs/), powered by [MkDocs](http://www.mkdocs.org/).

[Libretro Forums topic](https://forums.libretro.com/t/wip-adding-pages-to-documentation-site/10078)

![travis](https://www.travis-ci.org/libretro/docs.svg?branch=master)

## Building

1. Make sure you have [Python](https://www.python.org/) and [pip](https://pip.pypa.io) installed
    ```
    python --version
    pip --version
    ```

2. Install MkDocs
    ```
    pip install mkdocs
    ```

3. Install MkDocs-Material
    ```
    pip install mkdocs-material
    ```
	
4. Install PyMdown Extensions
    ```
    pip install pymdown-extensions
    ```	

5. Build the site
    ```
    mkdocs build
    ```

6. The documentation will be built to the `site` directory
