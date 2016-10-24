```sh
sudo zypper in patterns-openSUSE-devel_web php5-gd php5-mbstring php5-posix php5-zip php5-zlib
sudo zypper in php5-curl php5-fileinfo php5-bz2 php5-intl php5-mcrypt php5-openssl
sudo zypper in php5-APCu php5-exif php5-ftp php5-gmp php5-imap php5-imagick php5-pcntl
sudo zypper in php5-bcmath php5-calendar php5-dba php5-gettext php5-phar php5-shmop php5-sockets php5-soap php5-sysvmsg php5-sysvsem php5-sysvshm php5-wddx
```

Enable the modules `rewrite`, `headers`, `env`in YaST → HTTP-Server and set the options in the `Directory` section in the main host as follows:
```
AllowOverride All
Options All
```

*/srv/www/htdocs/owncloud/config/config.php*
```php
'apps_paths' => [
    [
        'path'=> '/srv/www/htdocs/owncloud/apps',
        'url' => '/apps',
        'writable' => false,
    ], [
        'path'=> '/home/benedikt9/Projekte/URZ',
        'url' => '/apps2',
        'writable' => true,
    ],
],
'memcache.local' => '\OC\Memcache\APCu',
```
