# Week 6: REST


## Lecture Material 

A new version of the following books have been released:

* [e516 Lecture Notes Engineering Cloud Computing, Gregor von Laszewski](https://laszewski.github.io/book/e516/) [@las19e516]
* [Cloud Computing, Gregor von Laszewski](https://laszewski.github.io/book/cloud/) [@las19cloudcomputing]
* [Chameleon Cloud](https://laszewski.github.io/book/chameleon/)
* [Introduction to Python for Cloud Computing, Gregor von Laszewski](https://laszewski.github.io/book/python/) [@las19python]

Go through Chapter **REST** of the 
[Cloud Computing](https://laszewski.github.io/book/cloud/)
[@las19cloudcomputing] book. This chapter includes,

* An introduction to REST
* An overview of frameworks using REST
* An overview of OpenAPI and how it relates to REST
* An introduction of using GitHub which is also a REST service from a
  Python API.

The chapter als includes a section on OpenAPI2 and Eve which is however
for this class not relevant.

## Lab Activities 

Implement the REST service explained in the Section 
*OpenAPI REST Service via Introspection* in your local machine

* Complete the exercises:

    * OpenAPI.Conexion.1
    * OpenAPI.Conexion.2
    * OpenAPI.Conexion.3
    * OpenAPI.Conexion.4
    * OpenAPI.Conexion.5 

* Complete the exercises:

    * E.OpenAPI.1
    * E.OpenAPI.2
    * E.OpenAPI.3
    * E.OpenAPI.4
    * E.OpenAPI.5 

## Graded Lab Activity

In this lab activity you will be adding more functionality to the REST
cpu example and deploying the service in the Chameleon Cloud.

You may need to install 
[py-cpuinfo](https://pypi.org/project/py-cpuinfo/0.2.3/) 
library to help you collect information for the service implementation. 

1. Change the *cpu* GET method, to work in a operating system invariant way
   (i.e. use python libraries to determine the CPU name, rather than system calls) 
   
1. Play around with *py-cpuinfo* library in Ubuntu environment just to get an 
    idea about the information you could retrieve. I suggest you spawn an Ubuntu 
    18.04 container on your local machine for this. 

1. Add a GET method to get cache size of the CPU. URL parameter *{level}* should 
  specify the cache level.        
  
    **GET http://localhost:8080/cloudmesh/cpu_cache/{level}**
  
    * level = 'l3' for l3 cache size
    * level = 'l2' for l2 cache size
   
   The return should be a dictionary as follows. 
   
   ```
   { 
       "l3" : "8448 KB"    
   } 
    ```
   
2. If cache level is not specified, the following dictionary should be returned. 
  
    ```
    { 
       "caches":{ 
          "l3":"8448 KB",
          "l2":"1024 KB"
       }
    } 
    ```
 
 3. Add these methods to the *cpu.yaml* definition. 
 
 4. Deploy the service locally and test the services using *swagger-UI*
    and curl.
 
 5. Create a **m1.small** instance in Chameleon Cloud with **ubuntu
    18.04** image. Deploy your new web service in the cloud instance.  You 
    should use *cloudmesh* commands to start these VMs. 
    
 6. Use curl to call the webservice in the cloud. (You are NOT expected to 
    expose the service through the public IP address)
    
 7. Capture the outputs for each service paths in a meaningful way
    (images, screenshots, etc) and compile a Markdown file. The Markdown
    should include, the new cpu.yaml file, server.py, and cpu.py files
    together with outputs. Furthermore, you should include the *cloudmesh* 
    commands that you have used in the process and you may include improvements 
    to the service such as handling malformed requests, etc.
 
 8. In the Markdown file, discuss what are the ways you could add
    security for these services (You do NOT need to implement this).
