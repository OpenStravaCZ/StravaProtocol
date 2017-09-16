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

| Code  | Description |
|-------|-------------|
| 0;    | OK          |
| 101;  | ERROR       |
| 1001; | ERROR       |

<hr>

### VerzeAplikace
App version. You can use any big number (n > ~1000 && n <= 2147483647) and you can verify supported version from [WSPovolenaVerzeA](#wspovolenaverzea)

<hr>

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
| [WSSeznamZarizeni](#wsseznamzarizeni)                       | Get info about institution|
| [WSSeznamZprav](#wsseznamzprav)                             | List of messages          |
| [WSStavKontaUzivatele](#wsskontauzivatele)                  | Get account balance       |
| [WSTestUzivatele](#wsstestuzivatele)                        |                           |
| [WSUlozVlastnostiUzivatele](#wsulozvlastnostiuzivatele)     | Save user information     |
| [WSUlozeniObjednavek](#wsulozeniobjednavek)                 | Save orders               |
| [WSZapisUdajeZarizeni](#wszapisudajezarizeni)               |                           |
| [WSZprava](#wszprava)                                       |                           |

### WSCasServeru
Get time from server
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

### WSPrihlaseniUzivatele
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

### WSPrihlaseniUzivateleI

### WSPrihlaseniUzivateleK

### WSRozpisBPlateb

### WSRozpisBVydeje

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
| Result     | String | XML about food menu. See [Food XML](#food-xml-wsrozpisobjednavek) |
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
| Result     | String | XML about food menu. See [Food XML](#food-xml-wsrozpisobjednavek) |
| Vysledek   | String | Result. See [Vysledek](#vysledek) section                         |
| XSDSchema  | String | Always "NE,NE". You can ignore this                               |
| Konto      | Double | Amount of money on account                                        |
| DatCas_akt | String | Last update. Format is DD. MM. YYYY h:mm:ss                       |

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
| Result   | String | None or [Institution info XML](#institution-info-xml-wsseznamzarizeni) |
| Vysledek | String | Result code. See [Vysledek](#vysledek) section                         |

### WSSeznamZprav

### WSStavKontaUzivatele

### WSTestUzivatele

### WSUlozVlastnostiUzivatele

### WSUlozeniObjednavek

### WSZapisUdajeZarizeni

### WSZprava

## Food XML (WSRozpisObjednavek)

### Specification
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="VFPData">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="rozpisobjednavek" maxOccurs="unbounded" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element type="xs:date" name="datum">
                                <xs:annotation>
                                    <xs:documentation>Date</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="druh">
                                <xs:annotation>
                                    <xs:documentation>Type of food. P = Soup, V = Dinner, Number = Food number for choice</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string " name="popisdruhu">
                                <xs:annotation>
                                    <xs:documentation>Type of food as full string</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="chod">
                                <xs:annotation>
                                    <xs:documentation>Dining operation. C = Normal food, E = Dinner, there are some unknown value</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:integer" name="pocet">
                                <xs:annotation>
                                    <xs:documentation>Number of ordered meals</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="nazevjidelnicku">
                                <xs:annotation>
                                    <xs:documentation>Food name</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:decimal" name="cena">
                                <xs:annotation>
                                    <xs:documentation>Price of food</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="omezeni">
                                <xs:annotation>
                                    <xs:documentation>Some unknown restriction, maybe allergens</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:integer" name="stav">
                                <xs:annotation>
                                    <xs:documentation>Some unknown state</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="datcas_kon">
                                <xs:annotation>
                                    <xs:documentation>Maximum time for checking in food</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="datcas_odh">
                                <xs:annotation>
                                    <xs:documentation>Maximum time for checking out food</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="polevka">
                                <xs:annotation>
                                    <xs:documentation>Soup indicator. A = It's soup, N = It's other food</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="popisjidelnicku">
                                <xs:annotation>
                                    <xs:documentation>Description of the menu</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="popis_al">
                                <xs:annotation>
                                    <xs:documentation>Allergens</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="popis_alz">
                                <xs:annotation>
                                    <xs:documentation>Allergens</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:sequence>
        </xs:complexType>
    </xs:element>
</xs:schema>
```

### Sample (One day)
```xml
<?xml version = "1.0" encoding="Windows-1252" standalone="yes"?>\n
<VFPData>\n\t
    <rozpisobjednavek>\n\t\t
        <datum>2017-09-20</datum>\n\t\t
        <druh>P</druh>\n\t\t
        <popisdruhu>polévka</popisdruhu>\n\t\t
        <chod/>\n\t\t
        <pocet>0</pocet>\n\t\t
        <nazevjidelnicku>Houbové kyselo</nazevjidelnicku>\n\t\t
        <cena>0</cena>\n\t\t
        <omezeni>B</omezeni>\n\t\t
        <stav/>\n\t\t
        <datcas_kon>9999-12-31T00:00:00</datcas_kon>\n\t\t
        <datcas_odh>9999-12-31T00:00:00</datcas_odh>\n\t\t
        <polevka>A</polevka>\n\t\t
        <popisjidelnicku/>\n\t\t
        <popis_al>01-Obiloviny obsahující lepek    \n06-Sójové boby (sója)            \n07-Mléko                         \n09-Celer                         \n</popis_al>\n\t\t
        <popis_alzk>01-Obiloviny obsahující lepek    \n06-Sójové boby (sója)            \n07-Mléko                         \n09-Celer                         \n</popis_alzk>\n\t
    </rozpisobjednavek>\n\t
    <rozpisobjednavek>\n\t\t
        <datum>2017-09-20</datum>\n\t\t
        <druh>1</druh>\n\t\t
        <popisdruhu>oběd 1</popisdruhu>\n\t\t
        <chod>C</chod>\n\t\t
        <pocet>1</pocet>\n\t\t
        <nazevjidelnicku>RÝŽOVÝ NÁKYP SE ŠVESTKAMI A MERUŇKAMI, SYPANÉ CUKREM, POLITÉ ŠŤÁVOU</nazevjidelnicku>\n\t\t
        <cena>29.00</cena>\n\t\t
        <omezeni>5E</omezeni>\n\t\t
        <stav>O</stav>\n\t\t
        <datcas_kon>2017-09-19T13:30:00</datcas_kon>\n\t\t
        <datcas_odh>2017-09-19T13:30:00</datcas_odh>\n\t\t
        <polevka>N</polevka>\n\t\t
        <popisjidelnicku/>\n\t\t
        <popis_al>03-Vejce                         \n07-Mléko                         \n</popis_al>\n\t\t
        <popis_alzk>03-Vejce                         \n07-Mléko                         \n</popis_alzk>\n\t
    </rozpisobjednavek>\n\t
    <rozpisobjednavek>\n\t\t
        <datum>2017-09-20</datum>\n\t\t
        <druh>2</druh>\n\t\t
        <popisdruhu>oběd 2</popisdruhu>\n\t\t
        <chod>C</chod>\n\t\t
        <pocet>0</pocet>\n\t\t
        <nazevjidelnicku>KRŮTÍ PLÁTEK S PÓRKEM A ČESNEKEM, BRAMBORY, ŠŤÁVA, RAJČE</nazevjidelnicku>\n\t\t
        <cena>29.00</cena>\n\t\t
        <omezeni>5E</omezeni>\n\t\t
        <stav>O</stav>\n\t\t
        <datcas_kon>2017-09-19T13:30:00</datcas_kon>\n\t\t
        <datcas_odh>2017-09-19T13:30:00</datcas_odh>\n\t\t
        <polevka>N</polevka>\n\t\t
        <popisjidelnicku/>\n\t\t
        <popis_al>01-Obiloviny obsahující lepek    \n07-Mléko                         \n</popis_al>\n\t\t
        <popis_alzk>01-Obiloviny obsahující lepek    \n07-Mléko                         \n</popis_alzk>\n\t
    </rozpisobjednavek>\n\t
    <rozpisobjednavek>\n\t\t
        <datum>2017-09-20</datum>\n\t\t
        <druh>3</druh>\n\t\t
        <popisdruhu>oběd 3</popisdruhu>\n\t\t
        <chod>C</chod>\n\t\t
        <pocet>0</pocet>\n\t\t
        <nazevjidelnicku>ZELENINOVÝ TALÍŘ - PEČIVO, BRAMBOROVÝ SALÁT</nazevjidelnicku>\n\t\t
        <cena>29.00</cena>\n\t\t
        <omezeni>5E</omezeni>\n\t\t
        <stav>O</stav>\n\t\t
        <datcas_kon>2017-09-19T13:30:00</datcas_kon>\n\t\t
        <datcas_odh>2017-09-19T13:30:00</datcas_odh>\n\t\t
        <polevka>N</polevka>\n\t\t
        <popisjidelnicku/>\n\t\t
        <popis_al>01-Obiloviny obsahující lepek    \n03-Vejce                         \n07-Mléko                         \n09-Celer                         \n10-Hořčice                       \n</popis_al>\n\t\t
        <popis_alzk>01-Obiloviny obsahující lepek    \n03-Vejce                         \n07-Mléko                         \n09-Celer                         \n10-Hořčice                       \n</popis_alzk>\n\t
    </rozpisobjednavek>\n\t
    <rozpisobjednavek>\n\t\t
        <datum>2017-09-20</datum>\n\t\t
        <druh>4</druh>\n\t\t
        <popisdruhu>oběd 4</popisdruhu>\n\t\t
        <chod>C</chod>\n\t\t
        <pocet>0</pocet>\n\t\t
        <nazevjidelnicku>KUNG PAO Z VEPŘOVÉHO MASA, JASMÍNOVÁ RÝŽE</nazevjidelnicku>\n\t\t
        <cena>29.00</cena>\n\t\t
        <omezeni>5E</omezeni>\n\t\t
        <stav>O</stav>\n\t\t
        <datcas_kon>2017-09-19T13:30:00</datcas_kon>\n\t\t
        <datcas_odh>2017-09-19T13:30:00</datcas_odh>\n\t\t
        <polevka>N</polevka>\n\t\t
        <popisjidelnicku/>\n\t\t
        <popis_al>01-Obiloviny obsahující lepek    \n03-Vejce                         \n05-Arašídy (podzemnice olejná)   \n06-Sójové boby (sója)            \n10-Hořčice                       \n</popis_al>\n\t\t
        <popis_alzk>01-Obiloviny obsahující lepek    \n03-Vejce                         \n05-Arašídy (podzemnice olejná)   \n06-Sójové boby (sója)            \n10-Hořčice                       \n</popis_alzk>\n\t
    </rozpisobjednavek>\n\t
    <rozpisobjednavek>\n\t\t
        <datum>2017-09-20</datum>\n\t\t
        <druh>V</druh>\n\t\t
        <popisdruhu>večeře 1</popisdruhu>\n\t\t
        <chod>E</chod>\n\t\t
        <pocet>0</pocet>\n\t\t
        <nazevjidelnicku>KUNG PAO Z VEPŘOVÉHO MASA, JASMÍNOVÁ RÝŽE</nazevjidelnicku>\n\t\t
        <cena>26.00</cena>\n\t\t
        <omezeni>5E</omezeni>\n\t\t
        <stav>O</stav>\n\t\t
        <datcas_kon>2017-09-19T13:30:00</datcas_kon>\n\t\t
        <datcas_odh>2017-09-19T13:30:00</datcas_odh>\n\t\t
        <polevka>N</polevka>\n\t\t
        <popisjidelnicku/>\n\t\t
        <popis_al>01-Obiloviny obsahující lepek    \n03-Vejce                         \n05-Arašídy (podzemnice olejná)   \n06-Sójové boby (sója)            \n10-Hořčice                       \n</popis_al>\n\t\t
        <popis_alzk>01-Obiloviny obsahující lepek    \n03-Vejce                         \n05-Arašídy (podzemnice olejná)   \n06-Sójové boby (sója)            \n10-Hořčice                       \n</popis_alzk>\n\t
    </rozpisobjednavek>\n\t
</VFPData>\n
```

## Institution info XML (WSSeznamZarizeni)

### Specification (Based on specification inside returned XML)
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="xs:schema">
        <xs:complexType>
            <xs:annotation>
                <xs:documentation>XSDSchema inside this XML that document VFPData (Total bullshit), you can ignore this xs:schema element while parsing</xs:documentation>
            </xs:annotation>
        </xs:complexType>
    </xs:element>
    <xs:element name="VFPData">
        <xs:complexType>
                <xs:choice maxOccurs="unbounded">
                    <xs:element name="pomizarizen_wsseznam" minOccurs="0" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:sequence>
                                <xs:element name="zarizeni">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="5"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Institution code</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="rezim_uzi">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="1"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>User right's identifier. S = Normal user</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="text_uziv">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="2147483647"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Arbitrary text supplied by institution</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="datcas_akt" type="xs:dateTime">
                                     <xs:annotation>
                                        <xs:documentation>Last update time</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="zas_obj">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="1"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Uknown identifier, always "A" for me</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="zas_vyd">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="1"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Uknown identifier, always "A" for me</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="zas_pla">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="1"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Uknown identifier, always "A" for me</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="text_anon">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="2147483647"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Arbitrary text supplied by institution</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="zeme">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="2"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Language in A2 format (http://www.worldatlas.com/aatlas/ctycodes.htm)</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_nazev">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="76"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Name of institution</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_ulice">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="38"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Street</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_mesto">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="38"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>City</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_psc">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="6"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>ZIP code of institution</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_telefon">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="38"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Phone number of instition</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_ucet">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="38"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Bank account of institution</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_email">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="60"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Email of instituion</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="v_url">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="128"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Institution website URL?</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="verze">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:decimal">
                                            <xs:maxLength value="5"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Application version (Not android app version). It's decimal number</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="pasivni_oi">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="1"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Some unknown state. It's always N for me</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="urlwsdl">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="254"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Looks like wsdl url, but it's unused</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="urlwsdl_s">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="254"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Looks like ssl wsdl url, but it's unused</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                                <xs:element name="android">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:maxLength value="1"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                    <xs:annotation>
                                        <xs:documentation>Looks, that it's unused</xs:documentation>
                                    </xs:annotation>
                                </xs:element>
                            </xs:sequence>
                        </xs:complexType>
                    </xs:element>
                </xs:choice>
            </xs:complexType>
    </xs:element>
</xs:schema>
```

### Sample
```xml
<?xml version = "1.0" encoding="Windows-1252" standalone="yes"?>\n
<VFPData>\n\t
    <xsd:schema id="VFPData"
        xmlns:xsd="http://www.w3.org/2001/XMLSchema"
        xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">\n\t\t
        <xsd:element name="VFPData" msdata:IsDataSet="true">\n\t\t\t
            <xsd:complexType>\n\t\t\t\t
                <xsd:choice maxOccurs="unbounded">\n\t\t\t\t\t
                    <xsd:element name="pomizarizen_wsseznam" minOccurs="0" maxOccurs="unbounded">\n\t\t\t\t\t\t
                        <xsd:complexType>\n\t\t\t\t\t\t\t
                            <xsd:sequence>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="zarizeni">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="5"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="rezim_uzi">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="text_uziv">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="2147483647"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="datcas_akt" type="xsd:dateTime"/>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="zas_obj">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="zas_vyd">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="zas_pla">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="text_anon">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="2147483647"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="zeme">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="2"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_nazev">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="76"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_ulice">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="38"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_mesto">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="38"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_psc">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="6"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_telefon">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="38"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_ucet">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="38"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_email">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="60"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="v_url">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="128"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="verze">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="5"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="pasivni_oi">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="urlwsdl">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="254"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="urlwsdl_s">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="254"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="android">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t
                            </xsd:sequence>\n\t\t\t\t\t\t
                        </xsd:complexType>\n\t\t\t\t\t
                    </xsd:element>\n\t\t\t\t
                </xsd:choice>\n\t\t\t\t
                <xsd:anyAttribute namespace="http://www.w3.org/XML/1998/namespace" processContents="lax"/>\n\t\t\t
            </xsd:complexType>\n\t\t
        </xsd:element>\n\t
    </xsd:schema>\n\t
    <pomizarizen_wsseznam>\n\t\t
        <zarizeni>2526</zarizeni>\n\t\t
        <rezim_uzi>S</rezim_uzi>\n\t\t
        <text_uziv>Vítejte na stránkách pro objednávání stravy naší jídelny.\n\n</text_uziv>\n\t\t
        <datcas_akt>2017-09-15T14:07:43</datcas_akt>\n\t\t
        <zas_obj>A</zas_obj>\n\t\t
        <zas_vyd>A</zas_vyd>\n\t\t
        <zas_pla>A</zas_pla>\n\t\t
        <text_anon>Pokud chcete využívat službu pro objednávání stravy po Internetu, informujte se v kanceláři ŠJ.\n</text_anon>\n\t\t
        <zeme>CZ</zeme>\n\t\t
        <v_nazev>SODEXO, s.r.o.</v_nazev>\n\t\t
        <v_ulice>Fr.Kupky 350</v_ulice>\n\t\t
        <v_mesto>Dobruška</v_mesto>\n\t\t
        <v_psc>518 01</v_psc>\n\t\t
        <v_telefon>494623416</v_telefon>\n\t\t
        <v_ucet>UCB : 496514004 / 2700</v_ucet>\n\t\t
        <v_email>provoz.dobruska.fms.cz@sodexo.com</v_email>\n\t\t
        <v_url/>\n\t\t
        <verze>4.58</verze>\n\t\t
        <pasivni_oi>N</pasivni_oi>\n\t\t
        <urlwsdl/>\n\t\t
        <urlwsdl_s/>\n\t\t
        <android/>\n\t
    </pomizarizen_wsseznam>\n
</VFPData>\n
```