# Food history XML

# Specification
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="VFPData">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="rozpisvydeje">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element type="xs:date" name="datum">
                                <xs:annotation>
                                    <xs:documentation>Food date</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="popisdruhu">
                                <xs:annotation>
                                    <xs:documentation>Food type as string</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="pocetobj">
                                <xs:annotation>
                                    <xs:documentation>Number of orders (by user)</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="pocetvyd">
                                <xs:annotation>
                                    <xs:documentation>Number of pick ups</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:dateTime" name="datumcasvydeje">
                                <xs:annotation>
                                    <xs:documentation>Pick up dateTime</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="nazevjidelnicku">
                                <xs:annotation>
                                    <xs:documentation>Name of food</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:date" name="kod_vydej">
                                <xs:annotation>
                                    <xs:documentation>Unknown identificator, not important, always "V" for me</xs:documentation>
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

# Sample
```xml
<?xml version = "1.0" encoding="Windows-1252" standalone="yes"?>\n
<VFPData>\n\t
    <rozpisvydeje>\n\t\t
        <datum>2017-09-06</datum>\n\t\t
        <popisdruhu>oběd 1</popisdruhu>\n\t\t
        <pocetobj>1</pocetobj>\n\t\t
        <pocetvyd>1</pocetvyd>\n\t\t
        <datumcasvydeje>2017-09-06T13:30:00</datumcasvydeje>\n\t\t
        <nazevjidelnicku>KYNUTÉ KNEDLÍKY S POVIDLY, CUKREM A MÁSLEM</nazevjidelnicku>\n\t\t
        <kod_vydej>V</kod_vydej>\n\t
    </rozpisvydeje>\n\t
    <rozpisvydeje>\n\t\t
        <datum>2017-09-08</datum>\n\t\t
        <popisdruhu>oběd 4</popisdruhu>\n\t\t
        <pocetobj>1</pocetobj>\n\t\t
        <pocetvyd>1</pocetvyd>\n\t\t
        <datumcasvydeje>2017-09-08T13:17:00</datumcasvydeje>\n\t\t
        <nazevjidelnicku>STUDENTSKÝ ŘÍZEK (salám Gothaj v těstíčku), BRAMBOROVÁ KAŠE, OKUREK</nazevjidelnicku>\n\t\t
        <kod_vydej>V</kod_vydej>\n\t
    </rozpisvydeje>\n\t
    <rozpisvydeje>\n\t\t
        <datum>2017-09-11</datum>\n\t\t
        <popisdruhu>oběd 1</popisdruhu>\n\t\t
        <pocetobj>1</pocetobj>\n\t\t
        <pocetvyd>1</pocetvyd>\n\t\t
        <datumcasvydeje>2017-09-11T13:25:00</datumcasvydeje>\n\t\t
        <nazevjidelnicku>DŘEVORUBCOVA VEČEŘE (bramborové špalíčky s cibulkou a slaninkou) - bezmasé</nazevjidelnicku>\n\t\t
        <kod_vydej>V</kod_vydej>\n\t
    </rozpisvydeje>\n\t
    <rozpisvydeje>\n\t\t
        <datum>2017-09-12</datum>\n\t\t
        <popisdruhu>oběd 2</popisdruhu>\n\t\t
        <pocetobj>1</pocetobj>\n\t\t
        <pocetvyd>1</pocetvyd>\n\t\t
        <datumcasvydeje>2017-09-12T13:20:00</datumcasvydeje>\n\t\t
        <nazevjidelnicku>ŠPAGETY BOLOGNESE S VEPŘOVÝM MASEM, SÝR</nazevjidelnicku>\n\t\t
        <kod_vydej>V</kod_vydej>\n\t
    </rozpisvydeje>\n\t
    <rozpisvydeje>\n\t\t
        <datum>2017-09-13</datum>\n\t\t
        <popisdruhu>oběd 2</popisdruhu>\n\t\t
        <pocetobj>1</pocetobj>\n\t\t
        <pocetvyd>1</pocetvyd>\n\t\t
        <datumcasvydeje>2017-09-13T13:21:00</datumcasvydeje>\n\t\t
        <nazevjidelnicku>DOMÁCÍ SEKANÁ PEČENĚ, BRAMBOROVÁ KAŠE, ZELNÝ SALÁT</nazevjidelnicku>\n\t\t
        <kod_vydej>V</kod_vydej>\n\t
    </rozpisvydeje>\n\t
    <rozpisvydeje>\n\t\t
        <datum>2017-09-15</datum>\n\t\t
        <popisdruhu>oběd 1</popisdruhu>\n\t\t
        <pocetobj>1</pocetobj>\n\t\t
        <pocetvyd>1</pocetvyd>\n\t\t
        <datumcasvydeje>2017-09-15T12:54:00</datumcasvydeje>\n\t\t
        <nazevjidelnicku>KRUPICOVÁ KAŠE S ČOKOLÁDOU, CUKREM A MÁSLEM</nazevjidelnicku>\n\t\t
        <kod_vydej>V</kod_vydej>\n\t
    </rozpisvydeje>\n
</VFPData>\n
```