## User info XML

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
        <xsd:complexType>
            <xsd:choice maxOccurs="unbounded">
                <xsd:element name="pomstravnik_wsvlastnosti" minOccurs="0" maxOccurs="unbounded">
                    <xsd:complexType>
                        <xsd:sequence>
                            <xsd:element name="ev_cislo">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:decimal">
                                        <xsd:totalDigits value="5"/>
                                        <xsd:fractionDigits value="0"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>User ID</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="zarizeni">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="5"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Institution code</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="karta">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="20"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Card number</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="jmeno">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="25"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Username</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="var_symbol">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="10"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Variable symbol</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="limit_prep">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:decimal">
                                        <xsd:totalDigits value="7"/>
                                        <xsd:fractionDigits value="2"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Unknown limit, maybe for loan</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="typ_dialb">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="1"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Unknown identifier</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="prezdivka">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="25"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Nickname</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="heslo">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="25"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>User password</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="email">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="100"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>User email</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="izpravy">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="15"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Special message for user</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="datcas_akt">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="20"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Last update</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="isk">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="1"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Unknown identifier</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="pdp">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="1"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Unknown identifier</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                            <xsd:element name="pov_zpravy">
                                <xsd:simpleType>
                                    <xsd:restriction base="xsd:string">
                                        <xsd:maxLength value="25"/>
                                    </xsd:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Unknown identifier</xs:documentation>
                                </xs:annotation>
                            </xsd:element>
                        </xsd:sequence>
                    </xsd:complexType>
                </xsd:element>
            </xsd:choice>
            <xsd:anyAttribute namespace="http://www.w3.org/XML/1998/namespace" processContents="lax"/>
        </xsd:complexType>
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
                    <xsd:element name="pomstravnik_wsvlastnosti" minOccurs="0" maxOccurs="unbounded">\n\t\t\t\t\t\t
                        <xsd:complexType>\n\t\t\t\t\t\t\t
                            <xsd:sequence>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="ev_cislo">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:decimal">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:totalDigits value="5"/>\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:fractionDigits value="0"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="zarizeni">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="5"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="karta">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="20"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="jmeno">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="25"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="var_symbol">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="10"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="limit_prep">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:decimal">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:totalDigits value="7"/>\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:fractionDigits value="2"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="typ_dialb">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="prezdivka">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="25"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="heslo">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="25"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="email">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="100"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="izpravy">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="15"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="datcas_akt">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="20"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="isk">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="pdp">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="1"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="pov_zpravy">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="25"/>\n\t\t\t\t\t\t\t\t\t\t
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
    <pomstravnik_wsvlastnosti>\n\t\t
        <ev_cislo>1111</ev_cislo>\n\t\t
        <zarizeni>2526</zarizeni>\n\t\t
        <karta>424242422</karta>\n\t\t
        <jmeno>Kuchař Josef</jmeno>\n\t\t
        <var_symbol>999999</var_symbol>\n\t\t
        <limit_prep>0.00</limit_prep>\n\t\t
        <typ_dialb/>\n\t\t
        <prezdivka>nickname</prezdivka>\n\t\t
        <heslo>password</heslo>\n\t\t
        <email>josef.kuchar267@gmail.com</email>\n\t\t
        <izpravy/>\n\t\t
        <datcas_akt>15. 9. 2017 14:07:43</datcas_akt>\n\t\t
        <isk>N</isk>\n\t\t
        <pdp>A</pdp>\n\t\t
        <pov_zpravy>OMP</pov_zpravy>\n\t
    </pomstravnik_wsvlastnosti>\n
</VFPData>\n
```