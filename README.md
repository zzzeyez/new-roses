# new-roses
![Screenshot 1](/screenshots/1.jpg)

Grab system-appearance/wallpaper selections from online sources.

## install

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

## Usage

`new-roses`, by default, applies a wallpaper from Unsplash.com and a color palette from Colorlovers.com with the search term "spring."  If no flags are provided then the argument will be treated as a search term.

```
Usage: new-roses [OPTION] [SEARCHTERM]
       [-u] [-c] [-b 'color'] [-l] [-w] [-s 'searchterm']
       [-d '/download/dir'] [-q] [-n] [-x] [-h]
       
Example: new-roses spring
         new-roses -b 222222 coffee
	 
Optional arguments:
  -u                      Apply wallpaper from Unsplash.com
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
