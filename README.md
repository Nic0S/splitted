# splitted

Split side-by-side photo scans into two separate image files on macOS.

`splitted` uses macOS's built-in `sips` command, so there is nothing extra to
install.

## Install

Open Terminal and run:

```sh
/bin/zsh -c "$(curl -fsSL https://raw.githubusercontent.com/Nic0S/splitted/main/install-splitted)"
```

Then close Terminal and open it again.

## Use

Go to the folder with your scans and run:

```sh
splitted
```

For example:

```sh
cd "/Users/you/Downloads/W319785"
splitted
```

The split photos will be saved in a sibling folder named `Splitted`.

Each input image creates:

```text
original_left.Tif
original_right.Tif
```

## Useful Options

```sh
splitted --dry-run   # preview what will happen
splitted --force     # overwrite existing split files
splitted --help      # show all options
```

Supported files: `jpg`, `jpeg`, `png`, `tif`, `tiff`, `heic`, `bmp`, `gif`.
