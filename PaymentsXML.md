# Payments XML
There are two versions of this XML, the first is with specification inside each request, the second one is without this specification inside (recommended)

## WSRozpisVydeje (With specification inside each request)

### Specification (Based on specification inside returned XML)
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="xsd:schema">
        <xs:complexType>
            <xs:annotation>
                <xs:documentation>XSDSchema inside this XML that document VFPData, you can ignore this xs:schema element while parsing</xs:documentation>
            </xs:annotation>
        </xs:complexType>
    </xs:element>
    <xs:element name="VFPData">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="rozpisplateb">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element type="xs:date" name="datum">
                                <xs:annotation>
                                    <xs:documentation>Date of payment</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:decimal" name="castka">
                                <xs:simpleType>
                                    <xs:restriction base="xs:decimal">
                                        <xs:totalDigits value="12"/>
                                        <xs:fractionDigits value="2"/>
                                    </xs:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Amount</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="popis">
                                <xs:simpleType>
                                    <xs:restriction base="xs:string">
                                        <xs:maxLength value="30"/>
                                    </xs:restriction>
                                </xs:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Payment description</xs:documentation>
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
                    <xsd:element name="rozpisplateb" minOccurs="0" maxOccurs="unbounded">\n\t\t\t\t\t\t
                        <xsd:complexType>\n\t\t\t\t\t\t\t
                            <xsd:sequence>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="datum" type="xsd:date"/>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="castka">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:decimal">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:totalDigits value="12"/>\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:fractionDigits value="2"/>\n\t\t\t\t\t\t\t\t\t\t
                                        </xsd:restriction>\n\t\t\t\t\t\t\t\t\t
                                    </xsd:simpleType>\n\t\t\t\t\t\t\t\t
                                </xsd:element>\n\t\t\t\t\t\t\t\t
                                <xsd:element name="popis">\n\t\t\t\t\t\t\t\t\t
                                    <xsd:simpleType>\n\t\t\t\t\t\t\t\t\t\t
                                        <xsd:restriction base="xsd:string">\n\t\t\t\t\t\t\t\t\t\t\t
                                            <xsd:maxLength value="30"/>\n\t\t\t\t\t\t\t\t\t\t
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
    <rozpisplateb>\n\t\t
        <datum>2017-09-05</datum>\n\t\t
        <castka>-120.00</castka>\n\t\t
        <popis>prodej čipu</popis>\n\t
    </rozpisplateb>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-05</datum>\n\t\t
        <castka>80.00</castka>\n\t\t
        <popis>hotově</popis>\n\t
    </rozpisplateb>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-05</datum>\n\t\t
        <castka>120.00</castka>\n\t\t
        <popis>platba za kartu nebo čip</popis>\n\t
    </rozpisplateb>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-07</datum>\n\t\t
        <castka>500.00</castka>\n\t\t
        <popis>běžný účet</popis>\n\t
    </rozpisplateb>\n
</VFPData>\n
```

## WSRozpisBVydeje

### Specification (Based on specification inside returned XML)
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="VFPData">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="rozpisplateb">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element type="xs:date" name="datum">
                                <xs:annotation>
                                    <xs:documentation>Date of payment</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:decimal" name="castka">
                                <xs:simpleType>
                                    <xs:restriction base="xs:decimal">
                                        <xs:totalDigits value="12"/>
                                        <xs:fractionDigits value="2"/>
                                    </xs:restriction>
                                </xsd:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Amount</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="popis">
                                <xs:simpleType>
                                    <xs:restriction base="xs:string">
                                        <xs:maxLength value="30"/>
                                    </xs:restriction>
                                </xs:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Payment description</xs:documentation>
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

### Sample
```xml
<?xml version = "1.0" encoding="Windows-1252" standalone="yes"?>\n
<VFPData>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-05</datum>\n\t\t
        <castka>-120.00</castka>\n\t\t
        <popis>prodej čipu</popis>\n\t
    </rozpisplateb>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-05</datum>\n\t\t
        <castka>80.00</castka>\n\t\t
        <popis>hotově</popis>\n\t
    </rozpisplateb>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-05</datum>\n\t\t
        <castka>120.00</castka>\n\t\t
        <popis>platba za kartu nebo čip</popis>\n\t
    </rozpisplateb>\n\t
    <rozpisplateb>\n\t\t
        <datum>2017-09-07</datum>\n\t\t
        <castka>500.00</castka>\n\t\t
        <popis>běžný účet</popis>\n\t
    </rozpisplateb>\n
</VFPData>\n
```