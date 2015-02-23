getRent methode
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
$rent = $gm->getRent(/* Hard coded rent id */, /* Account id */);

  var_dump($rent);

} catch (Exception $ex) {
  printf('<p class="pre">%s</p>', $ex->__toString());
}
```

## Return:

```
payload:
headers: NULL
postData:
url: <API url>
```

```
array(21) {
  ["id"] => int(74)
  ["name"] => string(25) "Lokalen St-Joris Turnhout"
  ["url"] => string(25) "lokalen-st-joris-turnhout"
  ["cjtid"] => int(0)
  ["mykey"] => string(40) " een sleutel"
  ["street"] => string(17) "straat"
  ["city"] => string(8) "stad"
  ["postcode"] => string(4) "post code"
  ["countrycode"] => string(2) "BE"
  ["postcodeid"] => string(4) "id van de post code"
  ["mail"] => string(21) "email adres"
  ["tel"] => string(13) "telefoon nummer"
  ["latlng"] => string(33) "51.3051977591932:4.94607925415039"
  ["link"] => string(49) "http://www.st-joris-turnhout.be/index.php/verhuur"
  ["cal"] => string(1) "y" ["nmax"]=> int(0)
  ["promo"] => string(159) "promo text"
  ["attest"] => string(1) "y or n"
  ["camp"] => string(1) "y or n"
  ["weekend"] => string(1) "y or n"
  ["party"] => NULL 
}
```
