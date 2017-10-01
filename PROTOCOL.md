# PROTOCOL

## Interfaces
There are two interfaces. The only difference is that one is HTTP and the second is HTTPS, so I will cover it as one

### HTTP Version
<https://www.strava.cz/istravne/WSiStravne/WSiStravne.wsdl>

### HTTPS Version (Recommended)
<https://www.strava.cz/iStravne/WSiStravneSSL/WSiStravneSSL.wsdl>

## WSDL SOAP Interface

<hr>

### Vysledek
Result codes

| Code  | Description             |
|-------|-------------------------|
| 0;    | OK                      |
| 101;  | ERROR                   |
| 1001; | ERROR                   |
| 2001; | Unsupported App version |

<hr>

### VerzeAplikace
App version. You can use any big number (n > ~1000 && n <= 2147483647) and you can verify supported version from [WSPovolenaVerzeA](#wspovolenaverzea)

<hr>

### List of Operations
| Name                                                        | Description                | SID Required |
|-------------------------------------------------------------|----------------------------|:------------:|
| [WSCasServeru](#wscasserveru)                               | Get time of server         | No           |
| [WSDemoUzivatel](#wsdemouzivatel)                           | Login as demo user         | No           |
| [WSJidArchiv](#wsjidarchiv)                                 |                            | No           |
| [WSJidArchivB](#wsjidarchivb)                               |                            | No           |
| [WSJidArchivObdobi](#wsjidarchivobdobi)                     |                            | No           |
| [WSJidelnicky](#wsjidelnicky)                               | Get food menu              | No           |
| [WSJidelnicky2](#wsjidelnicky2)                             | Get food menu              | No           |
| [WSJidelnickyA](#wsjidelnickya)                             | Get food menu              | No           |
| [WSJidelnickyB](#wsjidelnickyb)                             | Get food menu              | No           |
| [WSJidelnickyB2](#wsjidelnickyb2)                           | Get food menu              | No           |
| [WSJidelnickyBA](#wsjidelnickyba)                           | Get food menu              | No           |
| [WSNactiBVlastnostiUzivatele](#wsnactibvlastnostiuzivatele) | Load user information      | Yes          |
| [WSNactiVlastnostiUzivatele](#wsnactivlastnostiuzivatele)   | Load user information      | Yes          |
| [WSOdhlaseniUzivatele](#wsodhlaseniuzivatele)               | Logout user                | Yes          |
| [WSPovolenaVerzeA](#wspovolenaverzea)                       | Check app version          | No           |
| [WSPrihlaseniUzivatele](#wsprihlaseniuzivatele)             | Login user                 | No           |
| [WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea)           | Login user                 | No           |
| [WSPrihlaseniUzivateleE](#wsprihlaseniuzivatelee)           | Login user                 | No           |
| [WSPrihlaseniUzivateleI](#wsprihlaseniuzivatelei)           | Login user                 | No           |
| [WSPrihlaseniUzivateleK](#wsprihlaseniuzivatelek)           | Login user                 | No           |
| [WSRozpisBPlateb](#wsrozpisbplateb)                         | Get list of payments       | Yes          |
| [WSRozpisBVydeje](#wsrozpisbvydeje)                         | Get list of food history   | Yes          |
| [WSRozpisJObjednavek](#wsrozpisjobjednavek)                 | Get list of orders         | Yes          |
| [WSRozpisObjednavek](#wsrozpisobjednavek)                   | Get list of orders         | Yes          |
| [WSRozpisPlateb](#wsrozpisplateb)                           | Get list of payments       | Yes          |
| [WSRozpisVydeje](#wsrozpisvydeje)                           | Get list of food history   | Yes          |
| [WSS_OdeslaniMailu](#wssodeslanimailu)                      | Send email                 | Yes          |
| [WSS_OdeslaniMailu2](#wssodeslanimailu2)                    | Send email                 | Yes          |
| [WSS_OdeslaniSouboru](#wssodeslanisouboru)                  | Send a file                | Yes          |
| [WSS_OdeslaniSouboru_S](#wssodeslanisouborus)               | Send a file                | Yes          |
| [WSS_Odhlaseni](#wssodhlaseni)                              |                            | Yes          |
| [WSS_Prihlaseni](#wssprihlaseni)                            |                            | Yes          |
| [WSS_PrijemSouboru](#wssprijemsouboru)                      | Recieve a file             | Yes          |
| [WSS_PrijemSouboruMail](#wssprijemsouborumail)              | Recieve a file from email  | Yes          |
| [WSS_SmazaniSouboru](#wsssmazanisouboru)                    | Delete a file              | Yes          |
| [WSS_URLWSDL](#wssurlwsdl)                                  |                            | No           |
| [WSS_URLWSDL_S](#wssurlwsdls)                               |                            | No           |
| [WSS_VypisAdresare](#wssvypisadresare)                      | Directory listing          | Yes          |
| [WSSeznamBZprav](#wsseznambzprav)                           | List of messages           | Yes          |
| [WSSeznamPOZarizeni](#wsseznampozarizeni)                   | List of institutions       | No           |
| [WSSeznamPZarizeni](#wsseznampzarizeni)                     | List of institutions       | No           |
| [WSSeznamZarizeni](#wsseznamzarizeni)                       | Get info about institution | No           |
| [WSSeznamZprav](#wsseznamzprav)                             | List of messages           | Yes          |
| [WSStavKontaUzivatele](#wsskontauzivatele)                  | Get account balance        | Yes          |
| [WSTestUzivatele](#wsstestuzivatele)                        |                            | No           |
| [WSUlozVlastnostiUzivatele](#wsulozvlastnostiuzivatele)     | Save user information      | Yes          |
| [WSUlozeniObjednavek](#wsulozeniobjednavek)                 | Save orders                | Yes          |
| [WSZapisUdajeZarizeni](#wszapisudajezarizeni)               |                            | No           |
| [WSZprava](#wszprava)                                       |                            | Yes          |

### WSCasServeru
Get server time

#### Input
| Name          | Type   | Description                               |
|---------------|--------|-------------------------------------------|
| Vysledek      | String | Always empty                              |
| AutUzivatelWS | String | Always "ANDROID58"                        |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                 |
| CasServeru    | String | Always empty                              |

#### Result
| Name       | Type   | Description                                      |
|------------|--------|--------------------------------------------------|
| Result     | String | Always None                                      |
| Vysledek   | String | Result code. See [Vysledek](#vysledek) section   |
| CasServeru | String | Time of the server. Format is YYYY-MM-DDTh:mm:ss |

### WSDemoUzivatel
Login as demo user

### WSJidArchiv
Get food menu archive

### WSJidArchivB
Get food menu archive

### WSJidArchivObdobi
Get food menu archive from specific period

### WSJidelnicky
Get current food menu for specific institution

### WSJidelnicky2
Get current food menu for specific institution

### WSJidelnickyA
Get current food menu for specific institution

### WSJidelnickyB
Get current food menu for specific institution

### WSJidelnickyB2
Get current food menu for specific institution

### WSJidelnickyBA
Get current food menu for specific institution

### WSNactiBVlastnostiUzivatele
Get user information

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | None or [User info XML](UserInfoXML.md)        |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSNactiVlastnostiUzivatele
Get user information (With specification inside each request)

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | None or [User info XML](UserInfoXML.md)        |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSOdhlaseniUzivatele
Logout user

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | Always None                                    |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSPovolenaVerzeA
Check if app version is OK

#### Input
| Name          | Type   | Description |
|---------------|--------|-------------|
| Vysledek      | String | Always None |
| VerzeAplikace | String | App version |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | None or True                                   |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSPrihlaseniUzivatele
Login user

Seems broken. Use [WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) instead

### WSPrihlaseniUzivateleA
Login user

#### Input
| Name          | Type   | Description                                              |
|---------------|--------|----------------------------------------------------------|
| Vysledek      | String | Always None                                              |
| AutUzivatelWS | String | Always "ANDROID58"                                       |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                |
| Zarizeni      | String | Code of institution                                      |
| Uzivatel      | String | Username                                                 |
| Heslo         | String | Password                                                 |
| Email         | String | Always None                                              |
| VerzeAplikace | String | App version, see [VerzeAplikace](#verzeaplikace) section |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | None or SID + Login message, separated with ;  |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSPrihlaseniUzivateleE
Login user

### WSPrihlaseniUzivateleI
Login user

### WSPrihlaseniUzivateleK
Login user

### WSRozpisBPlateb
Get payment history

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | None or [Payments XML](PaymentsXML.md)         |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSRozpisBVydeje
Get food history info

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |
| Konto         | Double | Always "0"                                                                    |
| DatCas_akt    | String | Always None                                                                   |

#### Result
| Name       | Type   | Description                                    |
|------------|--------|------------------------------------------------|
| Result     | String | None or [Food history XML](FoodHistoryXML.md)  |
| Vysledek   | String | Result code. See [Vysledek](#vysledek) section |
| Konto      | Double | Amount of money on account                     |
| DatCas_akt | String | Last update. Format is DD. MM. YYYY h:mm:ss    |

### WSRozpisJObjednavek
Get food menu specific for user with specified language

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |
| XSDSchema     | String | Always "NE,NE"                                                                |
| Konto         | String | Always "0"                                                                    |
| DatCas_akt    | String | Always None                                                                   |
| Jazyk         | String | Language, Format is [A2](http://www.worldatlas.com/aatlas/ctycodes.htm)       |

#### Result
| Name       | Type   | Description                                                       |
|------------|--------|-------------------------------------------------------------------|
| Result     | String | XML about food menu. See [Foods XML](FoodsXML.md)                 |
| Vysledek   | String | Result. See [Vysledek](#vysledek) section                         |
| XSDSchema  | String | Always "NE,NE". You can ignore this                               |
| Konto      | Double | Amount of money on account                                        |
| DatCas_akt | String | Last update. Format is DD. MM. YYYY h:mm:ss                       |

### WSRozpisObjednavek
Get food menu specific for user

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |
| XSDSchema     | String | Always "NE,NE"                                                                |
| Konto         | String | Always "0"                                                                    |
| DatCas_akt    | String | Always None                                                                   |

#### Result
| Name       | Type   | Description                                                       |
|------------|--------|-------------------------------------------------------------------|
| Result     | String | XML about food menu. See [Foods XML](FoodsXML.md)                 |
| Vysledek   | String | Result. See [Vysledek](#vysledek) section                         |
| XSDSchema  | String | Always "NE,NE". You can ignore this                               |
| Konto      | Double | Amount of money on account                                        |
| DatCas_akt | String | Last update. Format is DD. MM. YYYY h:mm:ss                       |

### WSRozpisPlateb
Get payments history (With specification inside each request)

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | None or [Payments XML](PaymentsXML.md)         |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSRozpisVydeje
Get food history (With specification inside each request)

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |
| Konto         | Double | Always "0"                                                                    |
| DatCas_akt    | String | Always None                                                                   |

#### Result
| Name       | Type   | Description                                    |
|------------|--------|------------------------------------------------|
| Result     | String | None or [Food history XML](FoodHistoryXML.md)  |
| Vysledek   | String | Result code. See [Vysledek](#vysledek) section |
| Konto      | Double | Amount of money on account                     |
| DatCas_akt | String | Last update. Format is DD. MM. YYYY h:mm:ss    |

### WSS_OdeslaniMailu
Send email

### WSS_OdeslaniMailu2
Send email

### WSS_OdeslaniSouboru
Send file

### WSS_OdeslaniSouboru_S
Send file

### WSS_Odhlaseni

### WSS_Prihlaseni

### WSS_PrijemSouboru

### WSS_PrijemSouboruMail

### WSS_SmazaniSouboru

### WSS_URLWSDL

### WSS_URLWSDL_S

### WSS_VypisAdresare

### WSSeznamBZprav

### WSSeznamPOZarizeni

### WSSeznamPZarizeni

### WSSeznamZarizeni
Get instituion information

#### Input
| Name          | Type   | Description               |
|---------------|--------|---------------------------|
| Vysledek      | String | Always None               |
| AutUzivatelWS | String | Always "ANDROID58"        |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV" |
| Zarizeni      | String | Institution code          |

#### Result
| Name     | Type   | Description                                                            |
|----------|--------|------------------------------------------------------------------------|
| Result   | String | None or [Institution info XML](InstitutionInfoXML.md)                 |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section                         |

### WSSeznamZprav

### WSStavKontaUzivatele

### WSTestUzivatele

### WSUlozVlastnostiUzivatele

### WSUlozeniObjednavek
Save orders

#### Input
| Name          | Type   | Description                                                                   |
|---------------|--------|-------------------------------------------------------------------------------|
| Vysledek      | String | Always None                                                                   |
| AutUzivatelWS | String | Always "ANDROID58"                                                            |
| AutHesloSW    | String | Always "gQaUdg6H0eb2xXBV"                                                     |
| SID           | String | See [result of WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea) how to get it |
| XMLObjednavky | String | Orders. Look at [Orders XML](OrdersXML.md) for more                           |

#### Result
| Name     | Type   | Description                                    |
|----------|--------|------------------------------------------------|
| Result   | String | Always None                                    |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section |

### WSZapisUdajeZarizeni

### WSZprava