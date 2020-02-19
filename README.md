# urlview-weechat

This is a simple [weechat](https://weechat.org/) plugin that allows you
to pipe buffers through [urlview](https://github.com/sigpipe/urlview) or
[urlscan](https://github.com/firecat53/urlscan).
This gives you an interactive list of URLs to open, which is especially
helpful if there are multiple URLs in the buffer making
[urlgrab](https://weechat.org/scripts/source/urlgrab.py.html/) hard to
use.

## Installation

Copy the script to `~/.weechat/python/`

If you want it to be loaded when you start weechat, you must then link to it
from `~/.weechat/python/autoload/`

```sh
mkdir -p ~/.weechat/python/autoload
wget https://raw.githubusercontent.com/keith/urlview-weechat/master/urlview.py ~/.weechat/python/
cd ~/.weechat/python/autoload && ln -s ../urlview.py .
```

## Configuration

By default this script uses urlview to handle urls. To use urlscan, you can
set `plugins.var.python.urlview.command` to "urlscan".

To have email addresses removed before url parsing happens, you can set
`plugins.var.python.urlview.noemail` to true.

This is a python rewrite of [this ruby
plugin](https://weechat.org/files/scripts/unofficial/urlview.rb)
