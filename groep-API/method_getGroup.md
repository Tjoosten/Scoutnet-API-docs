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

```
Array (
  [accountid] => 332
  [accountname] => st-joris
  [groupname] => Sint-Joris
  [groupname2] => Scouts Turnhout
  [groupID] => A4107M
  [section] => Gouw Kempen - District Noorderkempen
  [hasaddress] => y
  [street] => Sint-Jorislaan 11
  [city] => Turnhout
  [postcode] => 2300
  [countrycode] => BE
  [postcodeid] => 2540
  [depname] => scoutnet.be
  [orgname] => Scouts en Gidsen Vlaanderen
  [orgid] => 1
  [mail] =>
  [tel] =>
  [latlng] => 51.3051977591932:4.94607925415039
  [urllist] => www.st-joris-turnhout.be
  [extra] => Array (
    [1] => Array (
      [zee] => n )

      [2] => Array (
        [akabe] => n
      )

      [3] => Array (
        [verhuur] => y
      )

      [4] => Array (
        [promo] =>
      )

      [5] => Array (
        [waar] =>
      )

      [6] => Array (
        [wanneer] => wanneer ?
      )

      [7] => Array (
        [lidgeld] =>
      )

      [8] => Array (
        [das] =>
      )
    )

  [sections] =>
    Array (
      [0] => Array (
        [section_name] => Kapoenen
        [section_code] => kapoenen
        [section_age] => 6,7,8
        [section_gender] => 2
      )

      [1] => Array (
        [section_name] => Welpen
        [section_code] => welpen
        [section_age] => 8,9,10,11
        [section_gender] => 1
      )

      [2] => Array (
        [section_name] => Jongverkenners
        [section_code] => jongverkenners
        [section_age] => 11,12,13
        [section_gender] => 1
      )

      [3] => Array (
        [section_name] => Jonggivers
        [section_code] => jonggivers
        [section_age] => 11,12,13
        [section_gender] => 2
      )

      [4] => Array (
        [section_name] => Givers
        [section_code] => givers
        [section_age] => 14,15,16
        [section_gender] => 2
      )

      [5] => Array (
        [section_name] => Jin
        [section_code] => jin
        [section_age] => 17,18
        [section_gender] => 2
      )
    )

    [types] => Array (
      [0] => Array (
        [type_name] => Lid
      )

      [1] => Array (
        [type_name] => Leiding
      )

      [2] => Array (
        [type_name] => Groepsleiding
      )

      [3] => Array (
        [type_name] => Stam
      )

      [4] => Array (
        [type_name] => Oudleiding
      )

      [5] => Array (
        [type_name] => Ouder
      )

      [6] => Array (
        [type_name] => VZW
      )

      [7] => Array (
        [type_name] => Oudercomite
      )

      [8] => Array (
        [type_name] => Webmaster
      )
    )
  ) 
```
