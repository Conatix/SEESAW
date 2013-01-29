Copyright (c) Conatix UK Ltd. www.conatix.com  
Stanbol Entity Set Acquisition Widget is a contribution of Conatix UK Ltd. to Apache Stanbol for the early adapters program of IKS, http://www.iks-project.eu/ SESAW is specifically built to fetch the pages from wikipedia, get the title and the URL of the respective title and add them to entityhub of the Apache Stanbol. When they're added to the entityhub, the entities can be used as Named Entities. It can be used to add entities for a language for instance. Another use of it is to add a category or a set of categories as well as portals.  
Author Amin Alizadeh, amin.alizadeh@conatix.com/amin.alizadeh@gmail.com

#Run the JAR file:  
java -jar seesaw.jar

args:  
(optional): If command line args are not used, the default configs.xml file is used. You can change the the properties in  configs.xml or create a new XML file under a new name. Note that the command line args override the XML or default values.

-URLs: the filename where the URLs are located in the XML format.  

-RDFFormat: Default is <http://www.w3.org/2000/01/rdf-schema#label>.

-Language: The language for the RDF request. The default value is Farsi (Persian).

-RDFFile: The RDF file where entities are stored in RDF Standard format. The default filename is persian-wiki.rdf.

-ValidateUrl: When fetching the pages from a list in Wikipedia, the addresses are relative. This will add the correct part at the beginning of the URL so they are valid URLs. The default value is http://fa.wikipedia.org

-EntityUrl: The entity where Apache Stanbol is installed. It ends with /entity/entityhub . The default value ishttp://dev.iks-project.eu:8081/entityhub/entity

-LogFile: LogFile is where the logs are stored. It logs in the result of the entity fetch and entity 

-RequestsPerSecond: The number of requests made per secondto the website from where the fetching and parsing is done.This is a politeness factor which limits the number of HTTPRequests to a website to avoid artificial traffic in the domain.

-RDFAppend: In the case the RDFFile already exists, you can append the entities to the file. This allows you to add them to the entityhub later.
