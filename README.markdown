# Introduction

This is a simple NPAPI test plugin with a scriptable (javascript) object. Any
function call into the plugin will return an int32 with the value 42.

## Build Process

In order to build this plugin you need to setup the NPAPI headers (e.g.
xulrunner-sdk) in *config.mk*.

After that just run `make`

Ubuntu splits up the xulrunner headers, that for you have to install 
*libnspr4-dev* and *xulrunner-dev* (at least on lucid) and add the following paths to *INCS* in *config.mk*:

<pre>
  -I/usr/include/xulrunner-1.9.2.17/ -I /usr/include/nspr
</pre>

Replace the xulrunner version by the version on your system. Alternatively you can download 
xulrunner 1.9.2.x from the [Gecko SDK download page](https://developer.mozilla.org/en/Gecko_SDK#Downloading).

## Supported Browsers

Following browsers have been tested successfully with this plugin so far:

- Iceweasel 2.0/Debian Linux
- Iceweasel 3.0/Debian Linux
- Firefox 2.0/Ubuntu Linux
- Firefox 3.0/Ubuntu Linux
- WebKit/GTK c6c3f8ca4996a96a1c7e9d1ddb9c6e3bd05daed9/Ubuntu Linux
- Opera 9.27/Ubuntu Linux
- Opera 9.5/Debian Linux
- Firefox 3/Darwin
- Safari 3.1.2/Darwin
- Firefox 3.0/Windows XP
- Opera 9.5/Windows XP
- Torchmobile's IRIS browser 1.0.13/Windows Mobile 6

What does not work:

- Opera 9.51/Darwin bug-350791@bugs.opera.com
