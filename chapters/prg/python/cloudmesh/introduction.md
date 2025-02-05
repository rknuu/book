# Introduction

---

![](images/learning.png) **Learning Objectives**

* Introduction to the cloudmesh API
* Using cmd5 via cms
* Introduction to cloudmesh convenience API for output, dotdict, shell, stopwatch, 
  benchmark management
* Creating your own cms commands
* Cloudmesh configuration file
* Cloudmesh inventory

---

In this chapter, we like to introduce you to cloudmesh which provides you
with a number of convenient methods to interface with the local system,
but also with cloud services. We will start while focussing on some
simple APIs and then gradually introduce the cloudmesh shell which not
only provides a shell but also a command line interface so you can use
cloudmesh from a terminal. This dual ability is quite useful as we can
write cloudmesh scripts, but can also invoke the functionality from the
terminal. This is quite an important distinction from other tools
that only allow command line interfaces.

Moreover, we also show you that it is easy to create new commands and add
them dynamically to the cloudmesh shell via simple pip installs. 

Cloudmesh is an evolving project and you have the opportunity to improve
if you see some features missing.

The manual of cloudmesh can be found at 

* <https://cloudmesh.github.io/cloudmesh-manual>

The API documentation is located at

* <https://cloudmesh.github.io/cloudmesh-manual/api/index.html#cloudmesh-api>

We will initially focus on a subset of this functionality.
