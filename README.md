Reusable Bash Scripts
=====================

[![Apache License Badge]][Apache License, Version 2.0]

### Cleaning all local docker containers, images, and volumes

```bash
curl -sL https://raw.githubusercontent.com/QubitPi/reusable-bash-scripts/refs/heads/master/docker-clean.sh | bash
```

### Add Paddings to Image

Adds paddings of an image to make it with certain dimension. To use this script, install ImageMagick first. For example,
on Mac, install by

```console
brew update
brew install imagemagick
```

> [!TIP]
>
> To install this script, place it under OS executable path. For example, On mac put this under "/usr/local/bin/"

The following examples assumes the input image is "input.png" and output image will be "output.png":

- Add _transparent_ paddings to make a _square image_ with the side being the larger one of original's width or height:

  ```console
  curl -sL https://raw.githubusercontent.com/QubitPi/reusable-bash-scripts/refs/heads/master/add-padding.sh | bash -s -- input.png output.png 
  ```

- Add _transparent_ paddings to make an image with dimension 1920x1080:

  ```console
  curl -sL https://raw.githubusercontent.com/QubitPi/reusable-bash-scripts/refs/heads/master/add-padding.sh | bash -s -- input.png output.png 1920x1080
  ```
  
- Add paddings, whose color is white, to make an image with dimension 1920x1080:


  ```console
  curl -sL https://raw.githubusercontent.com/QubitPi/reusable-bash-scripts/refs/heads/master/add-padding.sh | bash -s -- input.png output.png 1920x1080 white
  ```

### Keeps Executing A Command Util it Succeeds

```console
curl -sL https://raw.githubusercontent.com/QubitPi/reusable-bash-scripts/refs/heads/master/loop.sh | bash -s -- <command>
```

License
-------

The use and distribution terms for [reusable-bash-scripts]() are covered by the [Apache License, Version 2.0].

[Apache License Badge]: https://img.shields.io/badge/Apache%202.0-F25910.svg?style=for-the-badge&logo=Apache&logoColor=white
[Apache License, Version 2.0]: https://www.apache.org/licenses/LICENSE-2.0
