Casperjs module for Kohana PHP framework

====================================

Based on Alwex/php-casperjs 

Please read this documentation before usage:
[https://github.com/alwex/php-casperjs]


Added _toFile()_ method to save data to file

Basic usage:

At first at module to kohana modules list in application/bootstrap.php
```PHP
'casper'        => MODPATH.'phpcasperjs',    // Casperjs Module for Kohana
```

Then use in your controller:
```PHP
Casper::factory()
  ->start('http://yoururl-or-ip')
  ->fillFormSelectors('form', array('input[name="name"]' => 'user', 'input[name="password"]' => 'password' ), true)
  ->thenOpen('http://nexturl-or-ip')
  ->toFile('filename.html') 
  ->run(TRUE); //if set to TRUE will create infinite loop
```
