This project is a fork of [Arkitektum/GIS.Lib.MetadataCSW](https://github.com/Arkitektum/GIS.Lib.MetadataCSW), originally licensed under BSD-2-Clause.
The fork targets netstandard 2.0 and is compatible with .NET/.NET Core and .NET Framework 4.6.1+.
All modifications &copy; 2025 Statens kartverk.

This project contains code generated with xsd.exe for the ISO-19139 Metadata standard, together with the OGC Catalogue Service (CSW) standard.
These two standards together makes it possible to exchange geospatial metadata with the CSW-API.

The opengis xsd files are pretty complex and several patches has been applied to get the XSD-files compatible with .NET. 

Thanks to Yaron Naveh's work on getting the GML-schemas to work with .NET, see his blogpost here: 
http://webservices20.blogspot.no/2009/04/opengis-with-net-20-and-wcf.html

After the code was generated, even more patches has been applied to get the XML serialization correct. Primarly are these fixed to generic object fields where the xsd.exe tool is not able to figure out which types can be included. To avoid having 'xsi:type'-attributes all over the place, we have added extra annotations to the generated code.