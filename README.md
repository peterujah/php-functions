# php-functions
Wrapped all basic reusable php function which I always on on project


## Installation

Installation is super-easy via Composer:
```md
composer require peterujah/php-functions
```
## Usages

```php 
use \Peterujah\NanoBlock\Functions;
$func = new Functions();
```
Or extend the class and create your own new function like below.
```php
class MyFunction extends \Peterujah\NanoBlock\Functions{
  public function __construct(){
  }
  public function myFunction(){
    //do anything
  }
  public static function myStaticFunction(){
    //do anything
  }
}
```
And call initialize your custom class
```php
$func = new MyFunction();
```
