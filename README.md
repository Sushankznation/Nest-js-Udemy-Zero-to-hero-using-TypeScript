# Nest.js
----
## Decorators 
- In Nest.js, decorators are a key feature used for implementing various functionalities and 
adding metadata to classes, methods, properties, or parameters. Decorators are functions 
that can be attached to specific elements of a class to modify their behavior or provide additional information. 
They are commonly used for aspects like ```routing, validation, dependency injection```, and more. Decorators in Nest.js are based on the TypeScript decorator syntax.

Here are a few commonly used decorators in Nest.js:

- ```@Module```: Used to define a module in Nest.js. The @Module decorator is applied to a class and is responsible for organizing related providers, controllers, and other modules.

- ```@Controller```: Applied to a class, the @Controller decorator marks it as a controller. Controllers handle incoming requests, define routes, and contain methods decorated with HTTP method decorators.

- HTTP method decorators ```(@Get, @Post, @Put, @Delete, etc.)```: These decorators are applied to methods within a controller class and define the HTTP methods that the route will handle. They also specify the path for the route.

- ```@Injectable```: Used to mark a class as an injectable provider within the Nest.js dependency injection system. This decorator allows the class to be injected into other classes as a dependency.

- ```@Inject```: Applied to constructor parameters or properties within a class, the @Inject decorator specifies the dependency that should be injected into the parameter or property.

- ```@Param, @Query, @Body```: These decorators are used to extract data from the request parameters, query parameters, and request body, respectively. They are typically applied to method parameters within a controller to access and utilize the incoming data.

- ```@UseGuards, @UsePipes, @UseInterceptors```: These decorators are used to apply middleware, pipes, or interceptors to controllers or specific routes, enabling additional functionality such as authentication, data transformation, or error handling.

----
### Modules
- Each app has atleast one module, i.e, known as root module
- Modules are effective way to organize   components by a closely related set of capabilities(e.g per Feature)
- Its a good practice to have a folder  per module, containing the module ' components.
- Modules are singletons therefore a  module can be  imported by multiple other modules (promotes reusability, consistency, and efficient resource utilization)
- Command to create a module : ```nest g module name-of-module```
##### Defining a module 
- A module is defined by annotating a class  with the```@Module``` decorator
- Decorator provide the meta data
``` Metadata refers to data that provides information about other data. It offers context, description, and structure to help understand and manage the actual data it describes. In other words, metadata gives meaning and organization to raw data.```
----
##### Nest-js Controller :
 -  RResponsible for  handling incoming requests and returning  response of the client 
 - Bound to a specific path (eg. "/tasks") fot task resource. 
 - Contains handlers which handles endpoints and request methods like GET, POST, DELETE etc. 
 - Can take advantage of dependencies injection ot consume provider in the same module 
 - Defining Controller  