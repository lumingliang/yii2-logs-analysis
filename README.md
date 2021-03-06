Logs Analysis base Yii2 
========================

This Module Extension for Yii 2, Small teams, multi project development, testing model

For license information check the [LICENSE](LICENSE.md)-file.


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer.phar require dreamzml/yii2-logs-analysis
```

or add

```
"dreamzml/yii2-logs-analysis": "*"
```

to the require-dev section of your `composer.json` file.


Usage
-----

Once the extension is installed, simply modify your application configuration as follows:

```php
return [
    'modules' => [
        'analysis' => [
            'class'      => 'dreamzml\LogAnalysis\Module',
            'allowedIPs' => ['127.0.0.1', '::1'],          // if set ['*'] allow all ip
            'monitors'   => ['admin'=>'123456'],           //allow users, if set * allow all user
        ],
    ],
    // ...
];
```

You can then access Gii through the following URL:

```
http://localhost/path/to/index.php?r=analysis
```

or if you have enabled pretty URLs, you may use the following URL:

```
http://localhost/path/to/index.php/analysis
```
