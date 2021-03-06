CiAutoloading
========

Codeigniter PSR-0 compliant Autoloader hook for both Composer and "application/libraries" & "application/third_party". This is to be placed into "application/hooks" as a pre_system hook. See http://ellislab.com/codeigniter/user-guide/general/hooks.html for information on configuring hooks.

It is much better than placing it in the front controller of Codeigniter. Far more semantic. Since it is a pre_system hook, it runs before any major components of Codeigniter is loaded including the Router!

To install:

  * Enable hooks in ''config/config.php''.
  * In your ''config/hooks.php'' define:

```php
//pre_system autoloader
$hook['pre_system'] = array(
    'class' => 'Autoloader',
    'function'  => '__construct',
    'filename'  => 'Autoloader.php',
    'filepath'  => 'hooks',
);
```

  * Then download this into ''application/hooks/Autoloader.php''.