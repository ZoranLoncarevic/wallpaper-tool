# A simple tool to manage desktop wallpaper

The main purpose of this tool is to set a desktop wallpaper, like this

```bash
wallpaper set /path/to/image.filename
```

It can also apply a recipe given after the filename, in order to modify
this image on the fly (using imagemagick), darkening it or making it lighter,
blurring it, etc...

```bash
wallpaper set /path/to/image tint blur 10
```

When filename is omitted, the recipe applies to the current desktop
wallpaper, so that


```bash
wallpaper blur
```

replaces desktop wallpaper with a blurred version of itself. It cashes
these modified versions of image files under ~/.wallpaper directory.

There's a few more commands: `next`/`prev` sets the desktop wallpaper
to the next/previous image from the same directory, `shuffle`
chooses random image from the same directory, you can tag images
and then later select images using tags...

But beware, this was written for personal use so, for example, as is it
works only on GNOME desktops (it uses gsettings to set the wallpaper).
Furthermore, it was written as a sort of an exercise while learning
bash programming, so take it with a grain of salt.

To install it, just copy bash script somewhere in the `PATH`.
