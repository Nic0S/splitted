# splitted

`splitted` is a tiny macOS command for splitting scans that contain two photos
side by side.

It cuts each image vertically down the middle and writes two files:

```text
original_left.Tif
original_right.Tif
```

The script uses the built-in macOS `sips` command, so it does not require
Python, ImageMagick, Homebrew, or any other dependency.

## Quick Install

1. Open the Terminal app.
2. Paste this command and press Return:

```sh
/bin/zsh -c "$(curl -fsSL https://raw.githubusercontent.com/Nic0S/splitted/main/install-splitted)"
```

3. Close Terminal and open it again.
4. Type this and press Return:

```sh
splitted --help
```

If you see the help text, it worked.

## How To Split Photos

1. Open Terminal.
2. Type `cd ` with a space after it.
3. Drag your photo folder into the Terminal window.
4. Press Return.
5. Run:

```sh
splitted
```

That is it. Your split photos will be placed in a folder named `Splitted`.

For example, if your folder is:

```text
/Users/you/Downloads/W319785/High Res
```

then `splitted` will create:

```text
/Users/you/Downloads/W319785/Splitted
```

You can run it from the folder that contains the images:

```sh
cd "/Users/you/Downloads/W319785/High Res"
splitted
```

You can also run it from the parent folder:

```sh
cd "/Users/you/Downloads/W319785"
splitted
```

Both work.

## Try It Without Changing Anything

Use `--dry-run` to see what would happen before creating files:

```sh
splitted --dry-run
```

## If You Already Ran It Once

By default, `splitted` will not overwrite existing split photos.

To overwrite the old split photos, run:

```sh
splitted --force
```

## Other Install Option

If the quick install command feels too weird, you can download the project:

1. Open the GitHub page for this project.
2. Click the green **Code** button.
3. Click **Download ZIP**.
4. Double-click the ZIP file to unzip it.
5. Open Terminal.
6. Type `cd ` with a space after it.
7. Drag the unzipped `splitted` folder into Terminal.
8. Press Return.
9. Run:

```sh
./install-splitted
```

Close Terminal and open it again after installing.

## Useful Commands

```sh
splitted --help
splitted --dry-run
splitted --force
splitted --output "/path/to/Splitted" "/path/to/images"
```

## Supported Files

`splitted` looks for common image files:

```text
jpg, jpeg, png, tif, tiff, heic, bmp, gif
```

## Uninstall

To remove the command:

```sh
rm "$HOME/.local/bin/splitted"
```

You can also remove this line from `~/.zshrc` if you do not use it for anything
else:

```sh
export PATH="$HOME/.local/bin:$PATH"
```
