resourceGen
Author: John Dickinson
Copyright © 2015


Purpose
This tool is used to convert CSV comma delimited data into XML format for use with ArcSight. 

Always test your changes in a development system.


Features
Convert CSV formatted customer data
Convert CSV formatted category data
Convert CSV formatted location data
Convert CSV formatted network data
Convert CSV formatted zone data
Convert CSV formatted folder category data
Remove incompatible characters from source data
Normalize data

Installation
Unpack the zip file to any location on your hard drive
the zip will create a folder called resourceGen. 

Make sure java is in your path

The path below assumes you are using the ArcSight default java.

Linux:
PATH=$PATH:/opt/arcsight/console/current/jre/bin
export PATH

Windows:
set path=%path%;C:\arcsight\console\current\jre\bin

check your version of java
java -version
output should display Java Version 1.6 or higher

change to the resourceGen folder to execute the program
Usage: java -jar resourceGen.jar -n teS -xml zones.csv

-h          This help Message
-a          Display Author
-v          Display Version
-xml          convert to xml
-n          normalize {tesSmM}
    t   Title Case Words
    e   format spaces around data (data) {data} <data> data
    s   trim leading and trailing spaces around-and
    S   add leading and trailing spaces around - and
    m   add Start and Stop Address to Name when Stop Address supplied is bitmask
    M   add Start and Stop Address to Name when Stop Address supplied is subnet mask

Stop Address column can contain IP ei 192.168.1.0, bitmask ie /24 or subnet ei 255.255.255.0


Copyright © 2015 John Dickinson


