getRentIDs methode
=======================

## Vereiste param's

`account id` = `integer`


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
$rentids = $gm->getRentIDs(/* account id */);

  var_dump($rentids);
  return $rentids;

} catch (Exception $ex) {
  printf('<p class="pre">%s</p>', $ex->__toString());
}
```

## Return:

```
array(1) {
  [0]=> array(5) {
    ["accountid"] => string(3) "332"
    ["id"] => string(2) "74"
    ["name"] => string(25) "Lokalen St-Joris Turnhout"
    ["name_url"] => string(25) "lokalen-st-joris-turnhout"
    ["lastmod"] => string(19) "2014-11-11 21:25:42"
  }
}
```
