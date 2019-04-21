# new-roses
![Screenshot 1](/screenshots/1.jpg)

Grab system-appearance/wallpaper selections from online sources.

## Usage
Run `new-roses` with or without a search term to retrieve a wallpaper and system colorscheme.  
```
new-roses nature
```

Or, if you want to be more particular, then you can edit the config file at `~/.config/new-roses` or use one of the available flags:
```
Usage: new-roses [OPTION] [SEARCHTERM]
       [-a] [-u] [-c] [-b 'color'] [-l] [-w] [-s 'searchterm']
       [-d '/download/dir'] [-q] [-n] [-x] [-h]
       
Example: new-roses spring
         new-roses -b 222222 coffee
	 new-roses -wnq 
	 
Optional arguments:
  -a 'your_api_key'       Tell new-roses API key (creates config file).
  -u                      Apply wallpaper and color palette from Unsplash.com
  -c                      Apply color palette from Colorlovers.com
  -b 222222               Load colors directly from a colorscheme file.
  -l                      Use light color palette.
  -w			  Skip setting color palette.
  -s 'searchterm'         Use search term (if an argument with no flags is provided
			  it will be treated as a search term)
  -d '/path/to/dir/'	  Save wallpaper to directory.
  -q                      Quiet mode, don't print anything.
  -n			  Notify when finished (requires notify-send).
  -x                      Print all variables (test yr API connnection).
  -h			  Display this help page and exit.
```

## Installation
Download and place `new-roses` in your $PATH:
```
git clone https://github.com/zzzeyez/new-roses.git ~/Downloads/new-roses
mv ~/Downloads/new-roses/new-roses /usr/local/bin
```

And then install the depencies `jq` and `wal`:
```
brew install jq
pip3 install pywal
```

In order to fetch wallpaper images, you will need to obtain an Unsplash.com API key at https://unsplash.com/developers and then apply it to `new-roses` (this will create a config file at `~/.config/new-roses`):
```
new-roses -a 'YOUR_KEY_HERE'
```
