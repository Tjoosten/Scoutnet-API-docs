pingService methode
=======================

## Usage:

```php
$developer_key = ""; // jouw emailadres
$application_key = ""; // sn-nummer
$secret_key = ""; // Uw API sleutel
$debug = false // enable or disable debugging info;
require_once('Spinternet/Api.php');
try {
  $spinternet = Spinternet_Api::getInstance();
  $gm = $spinternet->getGroupManagement($developer_key, $application_key, $secret_key, $debug);
  $ping = $gm->pingService();

  var_dump($ping);

} catch (Exception $ex) {
  printf('<p class="pre">%s</p>', $ex->__toString());
}
```

## Return:

Return = 1 bij `TRUE` & 0 bij `FALSE`
