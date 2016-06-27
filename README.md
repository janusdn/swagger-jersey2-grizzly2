<!--
Copyright 2016 Janus Friis Nielsen

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

Swagger Jersey example using Grizzly Example
===================

This example demonstrates how to integrate Swagger with Jersey 2 running on Grizzly 2.

Contents
--------

The mapping of the URI path space is presented in the following table:

URI path                  | Resource class      | HTTP methods | Notes
--------------------      | ------------------- | ------------ | -------------------------------------------------------
**_/base/helloworld_**    | HelloWorldResource  |  GET         |  Returns `Hello World!`
**_/base/swagger.json_**  | _                   |  GET         |  Returns Swagger JSON

Running the Example
-------------------

Run the example as follows:

>     mvn clean compile exec:java

This deploys the example using [Grizzly](http://grizzly.java.net/) container.

-   <http://localhost:8080/base/helloworld>
-   <http://localhost:8080/base/swagger.json>


Notice
------

The example does not integrate the Swagger UI.

The example uses the library 'jersey-container-grizzly2-servlet' instead of the 'jersey-container-grizzly2-http' to get
the ServletConfig class required by Swagger.
