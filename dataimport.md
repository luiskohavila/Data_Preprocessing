## Data Importation
### Define the data table concept
Is display of information in tabular form, with rows and/or columns named. It is stored in, or derived from, a database.
### Define the data types

- **[Categorical](https://cloud.google.com/automl-tables/docs/data-types#categorical)**: Categorical value represents values in a category. That is, a nominal level. The values differ only based on their name without order. You can use numbers to represent categorical values, but the values have no numeric relationship with each other. That is, a categorical 1 is not "greater" than a categorical 0.

- **[Numeric](https://cloud.google.com/automl-tables/docs/data-types#numeric)**: A numeric value represents an ordinal or quantitative number. These numbers can be compared. That is, two distinct numbers can be less than or greater than one another.

- **Boolean**: Is a data type that has one of two possible values (true and false) which is intended to represent the two truth values of logic and Boolean algebra.

- **[Dates](https://cloud.google.com/automl-tables/docs/data-types#timestamp)**: A Timestamp value represents a point in time, represented either as a civil time with a time zone, or a Unix timestamp. Only features of type Timestamp can be used for the Time column. If a time zone is not specified with the civil time, it will default to UTC.

- **Strings**: Is used to represent text rather than numbers. It is comprised of a set of characters that can also contain spaces and numbers.

### Common data formats

- **[.csv](https://www.howtogeek.com/348960/what-is-a-csv-file-and-how-do-i-open-it/)**: A Comma Separated Values file is a plain text file that contains a list of data. These files are often used for exchanging data between different applications. These files mostly use the comma character to separate (or delimit) data, but sometimes use other characters, like semicolons.

- **[.json](https://fileinfo.com/extension/json)**: Is a file that stores simple data structures and objects in JavaScript Object Notation (JSON) format, which is a standard data interchange format. It is primarily used for transmitting data between a web application and a server. JSON files are lightweight, text-based, human-readable, and can be edited using a text editor.

- **[.xml](https://fileinfo.com/extension/xml)**: Is an XML (Extensible Markup Language) data file. It is formatted much like an .HTML document but uses custom tags to define objects and the data within each object. XML files can be thought of as a text-based database. It stores data in a structure that is machine-readable and human-readable.

- **[.xls](https://fileinfo.com/extension/xls)**: An XLS file is a spreadsheet file created by Microsoft Excel or another spreadsheet program. It contains one or more worksheets, which store and display data in a table format. Each worksheet included within a spreadsheet consists of a table with rows and columns and the cells in a table may contain manually entered data or the results computed from the data of other cells.

### Differentiate between local and remote repositories

- **[url](https://cornerstone.assembla.com/cornerstone/helpbook/pages/introduction/terminology/repositories.html)**: A remote URL is Git's is "the place where your code is stored." That URL could be your repository on GitHub, or another user's fork, or even on a completely different server. A URL uniquely describes the location of a resource on the Internet. Subversion uses URLs to identify items in a repository, with the URL at once identifying the server, repository and path of the file or folder in question.

- **[apis](https://schoolofdata.org/2013/11/18/web-apis-for-non-programmers/)**: API repository is a data access layer that defines a generic representation of a data store. API are stored in the Repository folders along with their associated management assets such as security policies and access control rules.

### [Identify the secure data transfer protocols](https://www.w3schools.in/types-of-network-protocols-and-their-uses/):

- **Transmission Control Protocol (TCP)**: Used for communicating over a network. It divides any message into series of packets that are sent from source to destination and there it gets reassembled at the destination.

- **Internet Protocol (IP)**: The IP addresses in packets help in routing them through different nodes in a network until it reaches the destination system.

- **User Datagram Protocol (UDP)**: UDP is a substitute communication protocol to Transmission Control Protocol implemented primarily for creating loss-tolerating and low-latency linking between different applications.

- **Post office Protocol (POP)**: POP3 is designed for receiving incoming E-mails.

- **Simple mail transport Protocol (SMTP)**: SMTP is designed to send and distribute outgoing E-Mail.

- **File Transfer Protocol (FTP)**: FTP allows users to transfer files from one machine to another..

- **Hyper Text Transfer Protocol (HTTP)**: Is designed for transferring a hypertext among two or more systems. HTML tags are used for creating links. These links may be in any form like text or images. HTTP is designed on Client-server principles which allow a client system for establishing a connection with the server machine for making a request.

- **Hyper Text Transfer Protocol Secure (HTTPS)**: Is a standard protocol to secure the communication among two computers one using the browser and other fetching data from web server. HTTP is used for transferring data between the client browser (request) and the web server (response) in the hypertext format, same in case of HTTPS except that the transferring of data is done in an encrypted format.

- **Telnet**: Telnet is a set of rules designed for connecting one system with another. The connecting process here is termed as remote login. The system which requests for connection is the local computer, and the system which accepts the connection is the remote computer.

- **Gopher**: Gopher is a collection of rules implemented for searching, retrieving as well as displaying documents from isolated sites.

### Describe the procedures for data importing

#### Import csv in Python:
```
from csv import reader
opened_file = open(data.csv')
read_file = reader(opened_file)
```
#### Import csv using pandas:
```
import pandas as pd
data = pd.read_csv("filename.csv")
```
#### Import file from URL using pandas:
```
import pandas as pd
mydata = pd.read_csv("http://winterolympicsmedals.com/medals.csv")
```
#### Import Text File:
```
import pandas as pd
mydata = pd.read_table("C:\\Users\\Deepanshu\\Desktop\\example2.txt")
```
#### Import Excel File:
```
import pandas as pd
mydata = pd.read_excel("https://www.eia.gov/dnav/pet/hist_xls/RBRTEd.xls",sheetname="Data 1", skiprows=2)
```
