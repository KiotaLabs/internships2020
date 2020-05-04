These are conceptual questions, and not programming tasks. In each of the following questions, we are looking for basic explanations, but please note that demonstrating with code examples wherever possible is the ultimate winning strategy. 
Name- Suyash Thonte (8484885935)
Email - suyashthonte0@gmail.com

### Data Serialization
1. What is the meaning of serialization (or deserialization) of Data?
	->> Serialization is a process of converting data or object to stream of bytes. This byte stream can be used for transmission of data or storage. This stream is platform independent, that means it can be run on any system and can be converted back to any desired form(i.e language).
   	->> Simliarly Deserialization is process of converting back this byte stream to the original object form/ data which can be run on the machine .
       	    - java.io.serializable interface is implemented to make object serializable.
       	    - writeObject() method is used for serialization and readObject() is used for deserialization. 


2. Name 3 frameworks or libraries which are most used for handling serialization in Java applications.
	->> - XSON
	    - GSON
	    - Azrael	
	    - Jackson


### Java Build Tools
As Java projects become bigger, they require build tools. Historically, Apache Ant, Maven and Gradle have been popular build tools. 
1. Why are build tools required?
	->> Build Tools are the tools which help in application development by automating the process of application creation.They are used to compiling, linking of various classes,etc and packaging the source code. In small projects manually building the throughout application is possible but 
	    In large projects, it is impossible to maintain a flow structure of build process also diffcult to keep track of the builded files. So These build tools are useful in 
	    -faster development of applications
	    -simplification and ease of building applications.
	    -managing and organizing your builds as well as maintain the proper connectivity.


2. What is the difference between Ant, Maven and Gradle?
	->> Ant was the first early build tool developed which used XML as build script.
		- Ant provided felxibility.
		- It provided build process control
		- Uses XML format being hierarchial, doesnt fit for procedural lanuages
	    Maven was later developed to overcome drawbacks of Ant.
		- It uses XML format but the structure is completely different.
		- It provided dependency download and management.
		- Dependency management doesnt handle the dispute between the different versions of library
	    Gradle is built up using combining both features of Ant and Maven.
		- It doesnt use XML script format instead uses its own domain specific language called as Groovy.
		- Due to this, Its scripts are shorter with less configuration.
		- Gradle is used as default build toll by Google.
 

### XML, JSON and REST
1. XML and JSON are two popular formats for storing or sharing data over networked applications. In most cases, these are the input or output formats of serialization (or deserialization) discussed above. 
2. What are some popular frameworks or libraries for handling XML and JSON data in Java. Name 2 for each. 
	->> JSON popular frameworks or libraries - 
		~ Jackson , GSON , JSON-lib.
	    XML libraries - 
		~ SAX parser, STAX parser, DOM parser, JAXB.


3. What is the purpose of making an API RESTful? In Java JAX RS is a popular standard for implementing REST principles. What are some popular libraries used for writing RESTful APIs in Java, preferably the ones which follow the JAX RS standard?
	->> - Making an API RESTful means to make it according to architecture of REST(Representational State Transfer), A RESTful API uses HTTP requests to execute these data transactions:GET,POST,PUT,DELETE
	    Using REST rather than the robust, complex SOAP makes data processing very simple as well as it uses less bandwidth which makes it efficient in net usage and can be flexibly implemented for cloud services.
	    REST has following characteristics : ~ Uniform interface
						 ~ Stateless Server-client protocol 
	    - Some libraries which implement Java JAX RS :
		~ Jersey
		~ Restet
		~ Apache CXF


4. What is the difference between websockets and HTTP based APIs?
	->> Websocket APIs :
		~ Overcomes drawback of HTTP by providing duplex communication
		~ Websockets used to transfer messages to client in real time 
		~ Bi-directional data/message transfer
		~ Due to real time updates faster then traditional HTTP.	
		~ Great for communication with high loads
	    
	    HTTP APIs : 
		~ HTTP implements REST architecture
		~ Due to this it provides the feature of Statelessness (Stateless Server-client protocol)
		~ Not bidirectional uses Request-Response messaging
		~ Great for occasional communication


### Dependency Injection
1. If you've used any Object Oriented Language, then you may have used constructors to instantiate an object of a class. Apart from constructors, dependency injection is another way of creating and providing objects, using something called Inversion of Control. What are some advantages of using Dependency Injection?
	->> Dependency Injection is a technique to implement IOC (inversion of control). DI is used to create dependent objects outside od its class using IOC.
	    Advanatges - 
		~ It makes easier to manage object dependencies.
		~ It implements Loose Coupling through IOC.
		~ It provides resusability, testability(in unit testing).
		~ It helps avoid the risk of changing the class by just changing its dependencies. 



2. Class dependencies can be injected using Annotations in Java, without the use of any external framework, however, frameworks make the implementation more convenient. Name two popular frameworks for implementing Dependency Injection in Java.
	->> - Spring is popular DI framework in Java
	    - Google Guice
	    - HK2


### Software Architecture
1. As you leave college and enter the software industry, you'll often encounter the phrase software architecture. It is used to refer to a broad number of things and the definition is not very crisp. We would request you to try and understand what it means. Here are a few links talking about architecture
    - https://martinfowler.com/architecture/
    - https://www.tutorialspoint.com/software_architecture_design/introduction.htm
    - https://towardsdatascience.com/10-common-software-architectural-patterns-in-a-nutshell-a0b47a1e9013

Share a small summary of what you understand from the above write ups. One of the tasks for our interns revolves around using and understanding the architecture of Hadoop YARN. 
	->> In the above links, Concept Of Software Architecure is discussed.So a software acrhitecure describes the major components of the system, their functioning, interconnectivity and thier relationships between them.In overall it represents the blue-print of the system.
	    Different acrhitectures can be developed based on functionality like layered pattern, server-client, MVC, data-flow ,component based,hieracrhial architectures,etc .In short Software acrhitecture converts characteristics like flexibility,scalability, reusability, etc into a structured framework that meets the technical and business expectations.
	    Comparing with Design, Architecture covers the bigger components of the system and how they function and interact whereas design refers to inner smaller structures of single software process.
	    YARN(Yet another resource manager) introduced in Hadoop 2.0.Hadoop 1.0 used Job tracker & task tracker in its arhitecure, while YARN uses Resource manager & node manager while mapreduce is just a processing engine.YARN implements resource management and job-scheduling tasks.
	    Compared to Hadoop 1.0's MapReduce's static resource alocation, YARN dynamically allocates resources to system as needed and which improves resource utilisation and performance.YARN consists of : - Resource Manager - Node manager - application master and container.


### Distributed Applications
1. What do you know about Hadoop? 
	->> Hadoop is a tool implemneted for Big Data Computing. Apache Hadoop is an open source framework for storing, processing and analysing massive amounts of multi-structured data in a distributed environment.
	   Hadoop consists of these modules - >> HDFS(Hadoop Distributed File System) which is storage for distributed file system. >> Map-Reduce model which a processing part which uses map-reduce programming paradigm for parallel processing of data. >> YARN a framework for effective resource management and job scheduling.

	
#### Google Cloud Bigtable
Bigtable is a distributed wide column store originally described in [this paper](https://static.googleusercontent.com/media/research.google.com/en//archive/bigtable-osdi06.pdf).

2. What is a wide column store?
	->> Wide Column store isa  type of No-SQL database.It is a 2-D key-value store.
	    A wide column store uses columns to store data.Related columns are grouped into column families. Rows are used to distinguish column families.
	    In a column family, the row key is its first column which identifies column family, later on column keys identify the column within that row.
	    Examples of wide column stores are Goole Big Table, Cassandra, HBASE


3. How is it different from column stores?  
	->> Wide column store stores data with ability to hold large no. of dynamic columns.Due to billions of columns and variable column names and row-keys it is seen as 2-D key value stores.


Apart from being massively distributed, Google Bigtable is also offered on the cloud as part of Google Cloud Platform.  

4. Are there equivalent cloud offerings from Microsoft Azure, Amazon Web Services, IBM and Oracle? If yes, what are their names?  
	->> - AWS offers Amazon Dynamo DB
	    - Oracle NoSQL offered by Oracle
	    - IBM dashDB/IBM db2 offered by IBM
	    - Azure Cosmos DB offered by Microsoft Azure


5. Are there open source alternatives to Google Cloud Bigtable, which can be self hosted? If yes, what are their names?
	->> Yes there are alternatives which can be self hosted like - SapphireDB, Oracle Db 10G.

