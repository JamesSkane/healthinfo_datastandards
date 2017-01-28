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