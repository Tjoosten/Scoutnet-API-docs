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

| Naam veld:             | Type veld:         | Description:                                                       |
| :--------------------- | :----------------- | :----------------------------------------------------------------- |
| `accountid`            | Integer            | De id van je account.                                              |
| `accountname`          | String             | De naam van je account.                                            |
| `groupname`            | String             | De naam van je groep.                                              |
| `groupname2`           | String             | Een alternatieve groepsnaam.                                       |
| `groupID`              | Integer            | De id van je groep.                                                |
| `section`              | String             | Onder Welke sectie je groep zit. bv: Gouw Antwerpen.               |
| `hasaddress`           | String             | y bij een address  anders een n van geen adres.                    |
| `street`               | String             | De straat waar je groep is gevestigd.                              |
| `city`                 | String             | De naam van het dorp, stad of gemeente waar je groep is gevestigd. |
| `postcode`             | String             | De postcode van de gemeente waar je groep is gevestigd.            |
| `countrycode`          | String             | De landscode.                                                      |
| `postcodeid`           | Integer            | De id van de postcode.                                             |
| `depname`              | String             | bv: scoutnet.be                                                    |
