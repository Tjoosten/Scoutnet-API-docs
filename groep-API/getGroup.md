getGroup methode:
============================

## Usage:

```php
$$developer_key = ""; // jouw emailadres
$application_key = ""; // sn-nummer  
$secret_key = ""; // Uw API sleutel
$debug = false; // enable or disable debugging info

require_once('Spinternet/Api.php');

try {
    $spinternet = Spinternet_Api::getInstance();
    $gm = $spinternet->getGroupManagement($developer_key, $application_key, $secret_key, $debug);
    //echo $gm->pingService();
    $group = $gm->getGroup(332);
    print_r($group);
    //var_dump($group);

} catch (Exception $ex) {
    printf('<p class="pre">%s</p>', $ex->__toString());
}
```
## Return:

| Naam veld:             | Type veld:         |
| ---------------------- | ------------------ |
| `accountid`            | Integer            |
| `accountname`          | String             |
| `groupname`            | String             |
| `groupname2`           | String             |
| `groupID`              | Integer            |
| `section`              | String             |
| `hasaddress`           | String             |
| `street`               | String             |
| `city`                 | String             |
| `postcode`             | String             |
| `countrycode`          | String             |
| `postcodeid`           | Integer            |
| `depname`              | String             |
