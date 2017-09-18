# Institution info XML

## Specification (Based on specification inside returned XML)
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

## Sample
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