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

## Available Static Methods

Make a random string/number
```php 
Functions::Random(10, Functions::INT);
```
Make a time ago from php timestamp, returns string
```php 
Functions::timeSocial(php_timestamp);
```
Generate a uuid string, returns string
```php 
Functions::uuid();
```

Verify a uuid string return true or false
```php 
Functions::is_uuid($uuid);
```

Verify email address is valid or not return true or false
```php 
Functions::is_email($email);
```

Create a password hash key
```php 
Functions::Encrypt($password);
```

Verify a password against hash key
```php 
Functions::Decrypt($password, $hash);
```

Calculate items average rating point
```php 
Functions::calcAverageRating($total_user_reviews, $total_rating_count);
```
Format number to money
```php 
Functions::Money($number, $fractional);
```
Create a tag/badge from array
```php 
Functions::badges(
    ["php", "js", "css"], 
    $bootstrap_color_without_prefix, 
    $type_of_badge, 
    $url_prefix_for_links
);
```

Create a button tag/badge from array
```php 
Functions::buttonBadges(
    ["php", "js", "css"], 
    $bootstrap_color_without_prefix, 
    $truncate, 
    $truncate_limit, 
    $selected_button_by_value
);
```

Returns user ip address
```php 
Functions::IP();
```
List time hours, returns array
```php 
Functions::hoursRange();
```

Secure/format user input based on required data type
```php 
Functions::XSS("Rhd53883773", "int");
```

Formats Convert string characters to HTML entities
```php 
Functions::htmlentities($string, $encode);
```

Copy files and folder to a new directory
```php 
Functions::copyFiles("path/from/file/", "path/to/file/");
```

Copy files and folder to a new directory
```php 
Functions::download(
    "path/to/download/file.zip", //string filepath to download
    "file.zip", // string file name to download
    false // bool delete file after download is complete true or false
);
```

Truncate text based on length
```php 
Functions::truncate(
    $text, //string text to truncate
    $length // int length to display
);
```
