# new-roses
![Screenshot 1](/screenshots/1.jpg)

Grab system-appearance/wallpaper selections from online sources.

## Install

Download and place `new-roses` in your $PATH:

```
git clone https://github.com/zzzeyez/new-roses.git ~/Downloads/new-roses
mv ~/Downloads/new-roses/new-roses /usr/local/bin
```

And then install the depencies `jq`, `imagemagick` and `wal`:

```
brew install jq imagemagick
pip3 install pywal
```

In order to fetch wallpaper images, you will need to obtain an Unsplash.com API key at https://unsplash.com/developers and then allow `new-roses` to use it:

```
touch ${HOME}/.config/api_keys
echo "unsplashapi=YOUR_API_KEY" > "${HOME/.config/api_keys"
```

## Usage

By default, a wallpaper from Unsplash and a color palette from Colorlovers are applied.  If no flags are provided, then any argument will be treated as a search term.  And if no flags or arguments are provided, then the search term "spring" and the background color "222222" will be used.  To use only Colorlovers or Unsplash use the -c or -u flags.

```
Usage: new-roses [OPTION] [SEARCHTERM]
       [-u] [-c] [-b 'color'] [-l] [-w] [-s 'searchterm']
       [-d '/download/dir'] [-q] [-n] [-x] [-h]
       
Example: new-roses spring
         new-roses -b 222222 coffee
	 new-roses -wnq 
	 
Optional arguments:
  -u                      Apply wallpaper and color palette from Unsplash.com
  -c                      Apply color palette from Colorlovers.com
  -b 222222               Load colors directly from a colorscheme file.
  -l                      Use light color palette.
  -w			  Skip setting color palette.
  -s 'searchterm'         Use search term (if an argument with no flags is provided
			  it will be treated as a search term)
  -d '/path/to/dir/'	  Save wallpaper to directory.
  -q                      Quiet mode, don't print anything.
  -n			  Notify when finished (requires `notify-send`).
  -x                      Print all variables (test yr API connnection).
  -h			  Display this help page and exit.
```
