# new-roses
![Screenshot 1](/screenshots/1.jpg)

grab wallpapers from unsplash

## use
run `new-roses` with or without a search term to retrieve a wallpaper
```
new-roses nature
```

an API key is required for now.  you can get one at unsplash.com and apply it with the -a flag

```
Usage: new-roses [OPTION] [SEARCHTERM]
       [-a] [-n] [-s ~/download/dir] 
       
Example: new-roses spring
	 
Optional arguments:
  -a 'your_api_key'       Tell new-roses API key (creates config file).
  -s '/path/to/dir/'	  Save wallpaper to directory.
  -n			          Notify when finished (requires notify-send).
  -h			          Display this help page and exit.
```

## installation
download and place `new-roses` in your $PATH:
```
git clone https://github.com/zzzeyez/new-roses.git ~/Downloads/new-roses
mv ~/Downloads/new-roses/new-roses /usr/local/bin
```

an API key from https://unsplash.com/developers must be applied:
```
new-roses -a 'YOUR_KEY_HERE'
```

and then install the depency `jq`
```
brew install jq
```
