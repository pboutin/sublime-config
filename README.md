Sublime Text 3 setup
==============

## Install the deb

> Source : http://www.sublimetext.com/3

## Inject the repository into the settings

```bash
cd ~/.config/sublime-text-3/Packages
rm -rf User
ln -s /path/to/repository/ User
```

## Install Package Control

In Sublime's console :

```python
import urllib.request,os,hashlib; h = '2deb499853c4371624f5a07e27c334aa' + 'bf8c4e67d14fb0525ba4f89698a6d7e1'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); urllib.request.install_opener( urllib.request.build_opener( urllib.request.ProxyHandler()) ); by = urllib.request.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); print('Error validating download (got %s instead of %s), please try manual install' % (dh, h)) if dh != h else open(os.path.join( ipp, pf), 'wb' ).write(by) 
```

> Source : https://packagecontrol.io/installation
