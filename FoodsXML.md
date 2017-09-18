# Foods XML

## Specification
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

## Sample (One day)
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