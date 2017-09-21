# Orders XML
There are two versions of this XML, the first is with specification inside each request, the second one is without this specification inside (recommended) 

## WSRozpisObjednavek (With specification inside each request)

### Specification (Based on specification inside returned XML)
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="xsd:schema">
        <xs:complexType>
            <xs:annotation>
                <xs:documentation>XSDSchema inside this XML that documents VFPData, just send this as in sample, this need more research</xs:documentation>
            </xs:annotation>
        </xs:complexType>
    </xs:element>
    <xs:element name="VFPData">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="rozpisobjednavek">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element type="xs:date" name="datum">
                                <xs:annotation>
                                    <xs:documentation>Food date</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element name="druh">
                                <xs:simpleType>
                                    <xs:maxLength value="1" />
                                </xs:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Type of food. P = Soup, V = Dinner, Number = Food number for choice</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element name="pocet">
                                <xs:simpleType>
                                    <xs:restriction base="xs:decimal">
                                        <xs:totalDigits value="5"/>
                                        <xs:fractionDigits value="0"/>
                                    </xs:restriction>
                                </xs:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Number of orders</xs:documentation>
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
<?xml version='1.0' encoding='Windows-1252' standalone='yes' ?>
<VFPData>
    <xsd:schema id="VFPData" 
        xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
        xmlns:msdata="urn:schemas-microsoft-com:xml-msdata">
        <xsd:element name="VFPData" msdata:IsDataSet="true">
            <xsd:complexType>
                <xsd:choice maxOccurs="unbounded">
                    <xsd:element name="rozpisobjednavek" minOccurs="0" maxOccurs="unbounded">
                        <xsd:complexType>
                            <xsd:sequence>
                                <xsd:element name="datum" type="xsd:date"/>
                                <xsd:element name="druh">
                                    <xsd:simpleType>
                                        <xsd:restriction base="xsd:string">
                                            <xsd:maxLength value="1"/>
                                        </xsd:restriction>
                                    </xsd:simpleType>
                                </xsd:element>
                                <xsd:element name="pocet">
                                    <xsd:simpleType>
                                        <xsd:restriction base="xsd:decimal">
                                            <xsd:totalDigits value="5"/>
                                            <xsd:fractionDigits value="0"/>
                                        </xsd:restriction>
                                    </xsd:simpleType>
                                </xsd:element>
                            </xsd:sequence>
                        </xsd:complexType>
                    </xsd:element>
                </xsd:choice>
                <xsd:anyAttribute namespace="http://www.w3.org/XML/1998/namespace" processContents="lax"/>
            </xsd:complexType>
        </xsd:element>
    </xsd:schema>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>2</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
</VFPData>
```

## WSRozpisBObjednavek

### Specification (Based on specification inside returned XML)
```xml
<?xml version="1.0" encoding="Windows-1252" standalone="yes"?>
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
    <xs:element name="VFPData">
        <xs:complexType>
            <xs:sequence>
                <xs:element name="rozpisobjednavek">
                    <xs:complexType>
                        <xs:sequence>
                            <xs:element type="xs:date" name="datum">
                                <xs:annotation>
                                    <xs:documentation>Food date</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element name="druh">
                                <xs:simpleType>
                                    <xs:maxLength value="1" />
                                </xs:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Type of food. P = Soup, V = Dinner, Number = Food number for choice</xs:documentation>
                                </xs:annotation>
                            </xs:element>
                            <xs:element name="pocet">
                                <xs:simpleType>
                                    <xs:restriction base="xs:decimal">
                                        <xs:totalDigits value="5"/>
                                        <xs:fractionDigits value="0"/>
                                    </xs:restriction>
                                </xs:simpleType>
                                <xs:annotation>
                                    <xs:documentation>Number of orders</xs:documentation>
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
<?xml version='1.0' encoding='Windows-1252' standalone='yes' ?>
<VFPData>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-18</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-19</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-20</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-21</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>1</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-22</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>2</druh>
        <pocet>1</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-25</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-26</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-27</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>1</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>2</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>3</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>4</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
    <rozpisobjednavek>
        <datum>2017-09-29</datum>
        <druh>V</druh>
        <pocet>0</pocet>
    </rozpisobjednavek>
</VFPData>
```