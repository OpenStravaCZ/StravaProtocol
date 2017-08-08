# PROTOCOL

## Interfaces
There are two interfaces. The only difference is that one is HTTP and the second is HTTPS, so I will cover it as one

### HTTP Version
<https://www.strava.cz/istravne/WSiStravne/WSiStravne.wsdl>

### HTTPS Version (Recommended)
<https://www.strava.cz/iStravne/WSiStravneSSL/WSiStravneSSL.wsdl>

## WSDL SOAP Interface

### List of Operations
| Name                                                        | Description               |
|-------------------------------------------------------------|---------------------------|
| [WSCasServeru](#wscasserveru)                               | Get time of server        |
| [WSDemoUzivatel](#wsdemouzivatel)                           | Login as demo user        |
| [WSJidArchiv](#wsjidarchiv)                                 |                           |
| [WSJidArchivB](#wsjidarchivb)                               |                           |
| [WSJidArchivObdobi](#wsjidarchivobdobi)                     |                           |
| [WSJidelnicky](#wsjidelnicky)                               | Get food menu             |
| [WSJidelnicky2](#wsjidelnicky2)                             | Get food menu             |
| [WSJidelnickyA](#wsjidelnickya)                             | Get food menu             |
| [WSJidelnickyB](#wsjidelnickyb)                             | Get food menu             |
| [WSJidelnickyB2](#wsjidelnickyb2)                           | Get food menu             |
| [WSJidelnickyBA](#wsjidelnickyba)                           | Get food menu             |
| [WSNactiBVlastnostiUzivatele](#wsnactibvlastnostiuzivatele) | Load user information     |
| [WSNactiVlastnostiUzivatele](#wsnactivlastnostiuzivatele)   | Load user information     |
| [WSOdhlaseniUzivatele](#wsodhlaseniuzivatele)               | Logout user               |
| [WSPovolenaVerzeA](#wspovolenaverzea)                       | Check app version         |
| [WSPrihlaseniUzivatele](#wsprihlaseniuzivatele)             | Login user                |
| [WSPrihlaseniUzivateleA](#wsprihlaseniuzivatelea)           | Login user                |
| [WSPrihlaseniUzivateleE](#wsprihlaseniuzivatelee)           | Login user                |
| [WSPrihlaseniUzivateleI](#wsprihlaseniuzivatelei)           | Login user                |
| [WSPrihlaseniUzivateleK](#wsprihlaseniuzivatelek)           | Login user                |
| [WSRozpisBPlateb](#wsrozpisbplateb)                         | Get list of payments      |
| [WSRozpisBVydeje](#wsrozpisbvydeje)                         | Get list of food history  |
| [WSRozpisJObjednavek](#wsrozpisjobjednavek)                 | Get list of orders        |
| [WSRozpisObjednavek](#wsrozpisobjednavek)                   | Get list of orders        |
| [WSRozpisPlateb](#wsrozpisplateb)                           | Get list of payments      |
| [WSRozpisVydeje](#wsrozpisvydeje)                           | Get list of food history  |
| [WSS_OdeslaniMailu](#wssodeslanimailu)                      | Send email                |
| [WSS_OdeslaniMailu2](#wssodeslanimailu2)                    | Send email                |
| [WSS_OdeslaniSouboru](#wssodeslanisouboru)                  | Send a file               |
| [WSS_OdeslaniSouboru_S](#wssodeslanisouborus)               | Send a file               |
| [WSS_Odhlaseni](#wssodhlaseni)                              |                           |
| [WSS_Prihlaseni](#wssprihlaseni)                            |                           |
| [WSS_PrijemSouboru](#wssprijemsouboru)                      | Recieve a file            |
| [WSS_PrijemSouboruMail](#wssprijemsouborumail)              | Recieve a file from email |
| [WSS_SmazaniSouboru](#wsssmazanisouboru)                    | Delete a file             |
| [WSS_URLWSDL](#wssurlwsdl)                                  |                           |
| [WSS_URLWSDL_S](#wssurlwsdls)                               |                           |
| [WSS_VypisAdresare](#wssvypisadresare)                      | Directory listing         |
| [WSSeznamBZprav](#wsseznambzprav)                           | List of messages          |
| [WSSeznamPOZarizeni](#wsseznampozarizeni)                   | List of institutions      |
| [WSSeznamPZarizeni](#wsseznampzarizeni)                     | List of institutions      |
| [WSSeznamZarizeni](#wsseznamzarizeni)                       | List of institutions      |
| [WSSeznamZprav](#wsseznamzprav)                             | List of messages          |
| [WSStavKontaUzivatele](#wsskontauzivatele)                  | Get account balance       |
| [WSTestUzivatele](#wsstestuzivatele)                        |                           |
| [WSUlozVlastnostiUzivatele](#wsulozvlastnostiuzivatele)     | Save user information     |
| [WSUlozeniObjednavek](#wsulozeniobjednavek)                 | Save orders               |
| [WSZapisUdajeZarizeni](#wszapisudajezarizeni)               |                           |
| [WSZprava](#wszprava)                                       |                           |

<hr>

### HARDCODED Inputs
| Name          | Type   | Value            |
|---------------|--------|------------------|
| AutUzivatelWS | String | ANDROID58        |
| AutHesloSW    | String | gQaUdg6H0eb2xXBV |
| Vysledek      | String |                  |
| CasServeru    | String |                  |

<hr>

### WSCasServeru
#### Input
| Name          | Type   | Description                               |
|---------------|--------|-------------------------------------------|
| Vysledek      | String | Always empty                              |
| AutUzivatelWS | String | See [HARDCODED Inputs](#hardcoded-inputs) |
| AutHesloSW    | String | See [HARDCODED Inputs](#hardcoded-inputs) |
| CasServeru    | String | Always empty                              |

#### Result
| Name       | Type   | Description                                      |
|------------|--------|--------------------------------------------------|
| Result     | String | Always None                                      |
| Vysledek   | String | See [Vysledek](#vysledek) section                |
| CasServeru | String | Time of the server. Format is YYYY-MM-DDTh:mm:ss |

### WSDemoUzivatel
### WSJidArchiv
### WSJidArchivB  
### WSJidArchivObdobi
### WSJidelnicky
### WSJidelnicky2
### WSJidelnickyA
### WSJidelnickyB
### WSJidelnickyB2
### WSJidelnickyBA
### WSNactiBVlastnostiUzivatele
### WSNactiVlastnostiUzivatele
### WSOdhlaseniUzivatele
### WSPovolenaVerzeA
### WSPrihlaseniUzivatele
### WSPrihlaseniUzivateleA
### WSPrihlaseniUzivateleE
### WSPrihlaseniUzivateleI
### WSPrihlaseniUzivateleK
### WSRozpisBPlateb
### WSRozpisBVydeje
### WSRozpisJObjednavek
### WSRozpisObjednavek
### WSRozpisPlateb
### WSRozpisVydeje
### WSS_OdeslaniMailu
### WSS_OdeslaniMailu2
### WSS_OdeslaniSouboru
### WSS_OdeslaniSouboru_S
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
### WSSeznamZprav
### WSStavKontaUzivatele
### WSTestUzivatele
### WSUlozVlastnostiUzivatele
### WSUlozeniObjednavek
### WSZapisUdajeZarizeni
### WSZprava