getAllEmailAliases methode
============================

## Vereiste param's

`account id` = ***integer***

## Usage:

```php
$developer_key = ""; // jouw emailadres
$application_key = ""; // sn-nummer
$secret_key = ""; // Uw API sleutel
$debug = false // enable or disable debugging info;
require_once('Spinternet/Api.php');
try {
  $spinternet = Spinternet_Api::getInstance();
   $am = $spinternet->getAccountManagement($developer_key, $application_key, $secret_key, $debug);

   //echo $am->pingService();
  $emailaliases = $am->getAllEmailaliases(/* account id */);

   print_r($emailaliases);
   //var_dump($emailaliases);

} catch (Exception $ex) {
  printf('<p class="pre">%s</p>', $ex->__toString());
}
```
## Return

```
Array ( [0] =>
  Array (
    [id] => integer
    [accountid] => integer
    [domainid] => integer
    [subdomainid] => integer
    [emailalias] => string
    [emailreal] => string
    [active] => integer
    [rem] =>
    [domain] => string
  )
)
```

De tweede `array` zal zich herhalen voor elke gebruiker.
