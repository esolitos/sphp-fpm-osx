# PHP-FPM version switcher for MacOS X

If you're on OSX with PHP and nginx installed via Brew, you may be looking for an easy way to switch between PHP-FPM (and PHP-cli) versions (5.3, 5.4, 5.5, 5.6, etc). For php-cli (and apache2) there is the well known sphp Well, this package is it.

Installation:

```
    # Create a /Users/yourname/Scripts dir (optional)
    mkdir ~/Scripts
    cd ~/Scripts
    git clone https://github.com/esolitos/sphp-fpm-osx.git
    # Link the script to the local bin dir 
    ln -s `pwd -P`/sphp-fpm-osx/sphpf /usr/local/bin/sphpf

```

Add `/usr/local/bin` to your `$PATH` if it's not already there.
If you use the Bash shell, you can do this by running this command:
```
    echo 'export PATH="/usr/local/bin:$PATH"' >> $HOME/.bashrc
```
You may need to restart your shell for this to take effect.

Usage:
```
    #: sphpf 54
    #: sphpf 55
    #: sphpf 56
    #: sphpf 70
```

## Troubleshooting

You can enable debug output simply setting `DEBUG` to true.

Example, enable for a single run:

    #: DEBUG=1 sphpf 70
    ...

Example, enable for the current shell:

    #: export DEBUG=1
    #: sphpf 70
    ...

## Thanks to

* Initial `sphp` by sgotre which inspired this script can be found at [sgotre/sphp-osx](https://github.com/sgotre/sphp-osx) 