# CGIC

## hello_world.cgi

Playing with CGI from C, since this is CGI everything can be run from the command line, but to run it via the webserver do the following (for apache at least)

### Build

```shell
$ make 
```

Will create `hello_world.cgi` in the same directory.

### Run

In the currently active site setup a directory to execute CGI

```apache
Alias /cgi-bin /var/www/cgi-bin
<Directory /var/www/cgi-bin>
    Options +ExecCGI
    AddHandler cgi-script .cgi
</Directory>
```

make sure mod cgi is loaded and enabled

```shell
$ a2enmod cgi
```

This will most likely enable cgid as apache is probably in threaded mode, but that is fine.

Now the CGI is accesible via the path `http://server/cgi-bin/hello_world.cgi`

