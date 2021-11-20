# Animal Shelter
####  Building an API. C# Project #6 - 11/6/21 


#### By Gabriel Ayala

## Technologies Used :floppy_disk:
* _C#_
* _LINQ_
* _NuGet Package Manager_
* _Entity_
* _Identity_
* _.Net 5 SDK_
* _REPL_
* _MySQL_
* _MySQL Workbench_
* _ASP.NET Core_
* _Git_
* _Swagger_



## Description :page_with_curl:
_A RESTful C# application that utilizes swagger to allow users to get, post, update, and delete objects within an api._

## Setup/Installation Requirements :triangular_ruler:

* _Clone github repo: https://github.com/Gabeaya/VendorOrder.Solution.git_
* _Navigate the directory: (cd top name directory)_
* _Open in Vs code: code ._
* _Run: dotnet restore AnimalShelter_
* _The line above will install necessary dependencies._
* _Next we will need a connection string: create a file within the main directory titled, "appsettings.json."_
* _Add the following within our new file: 
{
  "Logging": {
    "LogLevel": {
      "Default": "Warning",
      "Microsoft": "Information",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*",
  "ConnectionStrings": {
    "DefaultConnection": "Server=localhost;Port=3306;database=[YOUR-DATABASE-NAME-HERE];uid=[YOUR-USERNAME-HERE];pwd=[YOUR-PASSWORD-HERE];"
  }
}_
* _IMPORTANT NOTE: Do not iclude the brackets when entering your username or password._

* _Run: dotnet tool install --global dotnet ef --version 3.0.0 

* _Run: dotnet ef database update._

* _Run: dotnet run._

* _To utilize swagger copy and paste : http://localhost:5000_

* _Swagger allows you to view and generate client libraries within an api. Utilizing Swagger allows us to skip the step of writting our api endpoints within postamn by instead using a structured browser that has buttons for each endpoint._

## API Endpoints
* _Please open postman or another api platform in order to run these end points_


  - **[READ]** -- to view ALL animals, send a `GET` request to `/api/animals`
  - **[CREATE]** -- to create a new animal available at the shelter, send a `POST` request to `/api/animals`
    - you can insert the code below into the body as raw JSON, to create your animal with the `POST` method
  ```
      {
        "name": "{insert name}",
        "species": "{insert species type}",
        "age": "{insert age}",
        "gender": "{insert gender}",
        "date recieved": "{insert date}",
        "price": "{insert price}"
      }
  ```
  - **[READ]** -- to view a specific animal given an id, send a `GET` request to `/api/animal/{id}`
    - the {id} should be replaced by the specific id of the animal, without the curly brackets
  - **[UPDATE]** -- to update/edit a specific animal's information, send a `PUT` request to `/api/animals/{id}`
    - you can insert the code below into the body as raw JSON for editing the information
```
      {
        "name": "{insert name}",
        "species": "{insert species type}",
        "age": "{insert age}",
        "gender": "{insert gender}",
        "date recieved": "{insert date}",
        "price": "{insert price}"
      }
```
  - **[DELETE]** -- to delete an animal entry, locate the animal id you want to delete. Then send a `DELETE` request to `/api/animals/{id}`

## Parameters to a Get Request
You may add parameters to search for an animal with specific queries.

For example, if you wanted the animals returned to be filtered by a certain search criteria (e.g., all golden retrievers), you can type in the following url into the API request.

```
http://localhost:5000/api/animals?species=goldenretriever
```
You may also input multiple parameters by adding the & prior to the next query you'd like to combine the request with. This will return the one specific animal that matches each of the queries, as long as it exists. See the following code below.

```
http://localhost:5000/api/animals/?species=newfoundland&gender=female&name=nana
```




## License :clipboard:
MIT &copy; 2021 _Gabriel Ayala_
## Contact Information :mailbox:

_Gabriel Ayala:
gabeayala100@gmail.com_