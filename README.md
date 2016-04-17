# The Multi-Monitor Browser

This is a fullscreen Webkit based browser for kiosks and displays, with multi-monitor support.

## Install
To install you just need Python, [PyGTK](http://www.pygtk.org/) and [PyWebkitGtk](https://code.google.com/archive/p/pywebkitgtk/).

On Debian and Ubuntu, you just need to install :

```bash
sudo apt install python-webkit python-gtk2
```

And clone this repository:

```bash
git clone https://github.com/thor27/multimonitor-browser.git
```

## Usage

To run, you just need to execute the browser.py with an URL as argument:

```bash
./browser.py http://github.com/
```


If you have more than one monitor, you can run one URL for each monitor, for example:

```bash
./browser.py http://github.com/ http://www.python.org
```

Remember that you are locked in the hostname you called your script.
For example, this will not work:

```bash
./browser.py http://www.github.com/
```

It will print on terminal:

```bash
github.com not allowed host. Allowed hosts are: www.github.com.
```

To allow more than one host, you can use the **--allowed-hosts** argument, like that:

```bash
./browser.py http://www.github.com/ --allowed-hosts github.com
```

You can even allow more than one extra host:

```bash
./browser.py http://www.google.com/ --allowed-hosts github.com www.github.com www.python.org pypi.python.org
```

So you can search in google Github and Python and enter in those specifics sites. You may also need to add to **allowed-hosts** your regional Google site, for example **www.google.com.br**

You can also disable this, and allow any site navigation using **--allow-any-host**:

```bash
./browser.py http://www.google.com/ --allow-any-host
```

So now you can go to any website googles shows to you.

Also, by default, you can't close browser window. To change this behavior you need to use **--allow-close**:

```bash
./browser.py http://www.google.com/ --allow-close
```

## Contributors

* Thomaz de Oliveira dos Reis <thor27@gmail.com>

## License

* GPLv3
