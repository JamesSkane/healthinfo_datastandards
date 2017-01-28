#Data Standards 

Data standards - commonly accepted forms of recording data for the purpose of sharing, transmission, and exchange. 
* Lowest level CS standards:  **ASCII** and **UTF**-8 
    *  _allow computers the ability to share and display text information._
* Other data standards: **XML, HL7, JPEG**
   * _all of which are standards for encoding visual and audio media._
  
_________  
 
####Goal of Data Standards

The main goal of data standards is to ensure enough consistency that data from one system can be sent to another system 
for processing. 
Ideally, data standards ensure that the meaning of the data is captured and encoded in such a way that it is preserved 
as the data move between systems. In many cases, this is relatively simple as the data has a single, commonly understood 
meaning. In other cases, this becomes very difficult as the underlying data itself may contain multiple meanings.


_____
When defining data standards there is a trade off b/w **defining every little detail** (_thus making the standard very rigid and unable to adapt to new use cases or needs_), and being **very expressive** (_thus making the standard flexible and able to fit new needs but also making it extremely difficult to adhere to properly_).

A common approach when building software systems is to combine the piece parts in layers.
In the context of data standards, a particular standard may be built on top of other standards.

###### Example
 _- HL7 CDA documents are a data standard used within healthcare to transfer clinical information from one system to another. While the CDA is a healthcare-specific standard, it is built on top of a lower level standard known as XML._
 
 
 **HL7**'s new standard for exchanging healthcare information is known as **FHIR**.
 **_FHIR is built such that it can layer on top of XML or JSON_**, a commonly used standard in web applications. FHIR is currently only a draft standard and is being evaluated by HL7 and the general healthcare community. However, it is being created as a future alternative to current versions of HL7 such as the CDA. It is being embraced by many, including the Department of Health and Human Services
 
 
 # Why are Data Standards Necessary?
 Data standards form the basis for various computer **software systems to communicate data to one another**. Without data standards, systems would be unable to communicate or integrate each other, much like what we are currently experiencing in healthcare. Data standards provide the foundation on which complex systems can be built because they force various stakeholders and constituencies to agree upon how data is going to be shared.

One common standard that has dramatically increased the efficiency of businesses is the Portable Document Format, or PDF. Prior to PDFs, people typically sent around Word files. Inevitably, Word version 2000 was unable to read or edit files created in Word 2003, and vice versa. Even though everyone was using Microsoft Office, the lack of a clearly defined standard for shipping Word documents made it very difficult to preserve the proper formatting and layout. The introduction of PDF as a common standard made it trivial to send forms and other documents without worrying if the receiver was able to use it.

___
#JSON
From  
http://www.w3resource.com/JSON/introduction.php

"JSON is a lightweight text-based open standard data-interchange format. It is human readable. JSON is derived from a subset of JavaScript programming language (Standard ECMA-262 3rd Edition—December 1999). It is entirely language independent and can be used with most of the modern programming languages.

JSON is often used to serialize and transfer data over a network connection, for example between the web server and a web application. In computer science, serialization is a process to transforming data structures and objects in a format suitable to be stored in a file or memory buffer or transmitted over a network connection. Later on, this data can be retrieved. Because of the very nature of the JSON, it is useful for storing or representing semi structured data

JSON is a standard and is specified on RFC4627 on IETF (International Engineering Task Force). The specification is made by Doglus Crockford on July 2006.

JSON files are saved with .json extension. Internet media type of JSON is "application/json"."



    {
        "Title": "The Cuckoo's Calling",
        "Author": "Robert Galbraith",
        "Genre": "classic crime novel",
        "Detail": {
            "Publisher": "Little Brown",
            "Publication_Year": 2013,
            "ISBN-13": 9781408704004,
            "Language": "English",
            "Pages": 494
    },
    "Price": [
        {
            "type": "Hardcover",
            "price": 16.65
        },
        {
            "type": "Kidle Edition",
            "price": 7.03
        }
    ]
`

There four basic and built-in data types in JSON. They are strings, numbers, booleans (i.e true and false) and null. Besides, there are two data types which are structured - objects and arrays.
**Objects are wrapped within '{' and '}'**. **Arrays are enclosed by '[' and ']**'. **Objects** are a **list of label-value pairs**. **Arrays** are **list of values**.
Both objects and arrays can be nested.
strings, numbers, booleans (i.e true and false) and null can be used as values.


####

#XML
From http://www.w3schools.com/xml/
* XML stands for eXtensible Markup Language.
* XML was designed to store and transport data.
* XML was designed to be both human- and machine-readable.

See code in md to see how xml produced the text below:
<?xml version="1.0" encoding="UTF-8"?>
<note>
  <to>Tove</to>
  <from>Jani</from>
  <heading>Reminder</heading>
  <body>Don't forget me this weekend!</body>
</note>

      

_______
From http://www.ibm.com/developerworks/training/ondemandskills/

HTML tells how to present data while XML is a meta language, giving meaning to data that other applications can use. It provides information about information. Can be used with structured and unstructured data.
extensible. simpler version of SGML.

####XML Components
* Declaration - first line in document, contains 3 components:
    - Version: common
    - Encoding: defaults to UTF-8
    - Standalone: rare
* Tags: Text between < >, must have start and end tag, makes data self descriptive
* Elements: building blocks of XML file. text between the start and end tag. Documents contain 1 root element. Can contain nested elements
* Attributes: provide additional information about the elements. Name value pairs:
 Single or double quotes to encode values. Attribute names are unique within the same element
* Comments: <!-- comment --!>

Schemas - describe structure and content of XML document
standardized schemas are established based on industry
Core standards
Processing standards
Key vocabularies

Parsers read and process the contents of XML