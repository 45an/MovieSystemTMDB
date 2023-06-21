# MovieSystemTMDB 

![blue_short-8e7b30f73a4020692ccca9c88bafe5dcb6f8a62a4c6bc55cd9ba82bb2cd95f6c](https://github.com/45an/MovieSystemTMDB/assets/114033186/8147f2c5-38c6-4ac1-b96f-c4124930591e)


MovieSystemTMDB is a C# project that utilizes Minimal API, Entity Framework, and Microsoft SQL Server Management Studio (SSMS) to create a simple application for interacting with a database. 
The project provides a set of API endpoints that allow users to retrieve information about movies, genres, and users. 
Users can also establish connections between users and movies or genres. Additionally, the project includes functionality to add new movies to the database and facilitate movie discovery based on genres using TheMovieDB's API.

## Prerequisites

Before running the application, make sure you have the following:

    - .NET SDK installed
    - SQL Server database with a connection string configured in the appsettings.json file
    - TMDB API key
   
## 🔥 Features

    - API-based interaction with the database.
    - Retrieval of detailed information about users, genres, and movies.
    - Seamless connection of users to new movies and genres.
    - Easy addition of movies to expand the database.
    - Genre-based movie discovery for enhanced user experience.
    
## ⚙️ Technologies Used

👨‍💻 C#

🚀 ASP.NET: Minimal API. 

🛠️  Entity Framework 

📦 Microsoft SQL Server Management Studio (SSMS)

🖥️ Visual Studio IDE

🛌 Insomnia / Swagger: API test case management tool.

## 📑 API Endpoints and Data

The MovieSystemTMDB API provides the following endpoints and returns the associated data:

| API Endpoint | Returned Data|
| ------ | ------ |
| GET /api/DiscoverTitels/?GenreName={genreName} | Retrieves information about movies in a specific genre from the TMDB API. |
| GET /api/Person/ | Retrieves information about every person in the database.|
| GET /api/PersonGenre/?FirstName={firstName}| Retrieves the genres liked by a person. |
| GET /api/Person/GetMovies/{name}| Retrieves movies by person name. |
| GET /api/Person/GetGenres/{title}| Retrieves genres liked by a person. |
| GET /api/Genre/GetAll | Retrieves all genres. |
| GET /api/Persons/GetAll | Retrieves all persons. |
| GET /api/Person/GetRatings/{name}| Retrieves ratings on movies by person name. |
| POST /api/Movie/AddRating | Adds ratings to movies linked to a person. |
| POST /api/Person/AddGenre | Adds a genre to a person. |
| POST /api/Person/AddMovieLink | Adds a movie link to a specific person and genre. |
| GET /api/Person/GetMoviesGenre/{Titel} | Retrieves movies by person name including genre. |

## 📈 Code Structure 

| File/Folder | Description |
| ------ | ------ |
| Data | Contains the database context and migrations. |
| Models | Contains the model classes for the database entities.|
| Program.cs | Entry point for the application. |
| appsettings.json | Configuration file for the application. |
| MovieSystem.csproj | Project file for the C# project. |
| .gitignore | Specifies which files and folders to ignore in version control. |


## 🖳 Database Configuration

The application uses Entity Framework Core to connect to a SQL Server database.
The connection string can be configured in the appsettings.json file. 
Make sure to update the connection string to match your SQL Server database configuration.


