# Website CLI

Associate websites to directory paths to easily open them from the command line.

## Installation

Install [Go](https://golang.org/doc/install)

Clone, then: 
```
$ make && make install
```

You're ready to go!

## Usage

In the following snippets `[~/project1]` reperesents the current directory.

```
[~/project1] $ website add http://www.example.com
```

```
[~/project1] $ website list
http://www.example.com
```

Open the website in your browser:
```
[~/project1] $ website
```

You can optionally add a nickname for easy access:
```
[~/project1] $ website add http://www.github.com --name=github
[~/project1] $ website list
http://www.example.com
github (http://www.github.com)
[~/project1] $ website github  # Opens github in browser
```

If you add multiple sites to the same path you will be prompted to select one:
```
[~/project1] $ website add http://www.github.com
[~/project1] $ website
Please select:
  http://www.example.com
  http://www.github.com
```

Websites are associated with a particular path, so it is easy to add project websites to each path.
```
[~/project1] $ cd ~/project2
[~/project2] $ website add http://www.github/user
[~/project2] $ website list
http://www.github/user
```

## Uninstall

`make uninstall`
