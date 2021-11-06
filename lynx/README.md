# Big thanks to Rob Muhlestein (github.com/rwxrob) for making this config/setup


## Text Web Browser with CLI Search, Vim Bindings, GruvBox

Inspired by Robs setup. I loved his settings which includes:

* Vim bindings (which I really suck at but I'm trying to learn)
* GruvBox color theme (by far my favorite color scheme)
* Transparent background (works very well with my i3 setup)
* Accept Cookies (bloody annoying thing with Lynx)
* SSL Certificates Included
* Minimal interface
* Lies about User-Agent


# How I got this done

On Debian/Ubuntu ``` sudo apt install lynx ```. Then I had to place ``` lynx.cfg ``` and ``` lynx.lss `` into ``` /etc/lynx ```
I also placed scripts found in ``` bin ``` folder as well to take advantage of Rob's brilliant way to search the internet.

# Searching aliases

The ``` bin ``` folder we placed is what enables us to use the "?" to run a search. For example, if I want to search about a certain topic in Physics I would simply use ``` ? what is energy in physics ``` which will direct my search query to DuckDuckGo. "??" is for Google, and "???" for Bing. Apparently, DuckDuckGo is well optimized for Text-based web browsers and is my only way to go.

Place the code block below in your ``` .bashrc ``` file

``` 
alias '?'=/etc/lynx/bin/duck
alias '??'=/etc/lynx/bin/google
alias '???'=/etc/lynx/bin/bing

```
Dont forget to ``` source ~/.bashrc ``` for immediate results.
