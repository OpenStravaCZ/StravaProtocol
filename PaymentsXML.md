# Payments XML

## Specification
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
                                <xs:annotation>
                                    <xs:documentation>Amount</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element type="xs:string" name="popis">
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

## Sample
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