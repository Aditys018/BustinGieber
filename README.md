
# BustinGieber
## It is a music streaming android application 


## version control

#### connect android studio to GitHub


Create your GitHub Account here https://github.com/

Create a new project in your Android studio

to connect it with GitHub Create a new GitHub repo 

(Make sure Git and GitHub are installed from settings>properties>Plugin)

open the terminal in your Android Studio

Give the following Commands


| Command | Description|
| :--------  | :-------------------------------- |
|  cd/path/to/your/project   |  Change Directory to Your Project  |
| git init  | Initialize Empty Git Repository |
|  git add .  |  Add files to git |
| git commit -m "initial commit"  | Commit your changes |
|  git remote add origin (repo URL)  |  Add GitHub as remote  |
| git push -u origin master| Push your changes |



 
 
Steps to create the project

STEP 1 = Search for a better free music streaming API

STEP 2 = Add required dependencies

STEP 3 = Create Data Class

Step 4 = Create the API interface

Step 5 = Fetch data in main activity

Step 6 = UI/UX 


STEP 1 =

Go to this link  https://rapidapi.com/collection/music-apis
(make sure you are signed in)

We will be using Deezer API For this project

The link for the API IS   https://rapidapi.com/deezerdevs/api/deezer-1/

select kotlin OKHTTP
Test Endpoint checkout the keys and data
checkout the API here  https://jsonformatter.curiousconcept.com/#




STEP 2 = Adding the dependencies

we will be adding Retrofit dependency and GSON Converter in our project 

//retrofit dependency
visit link  https://square.github.io/retrofit/
(add latest version)

//GSON Converter
Visit link  https://github.com/google/gson
(add latest version)

Make sure to Sync the project

```http

 implementation ("com.squareup.retrofit2:retrofit:2.9.0")

 implementation ("com.squareup.retrofit2:converter-gson:2.9.0")

implementation("com.squareup.picasso:picasso:2.8")
```


STEP 3 = Create Data Class

Now we will convert JSON Data into data class

For that copy the data from https://rapidapi.com/deezerdevs/api/deezer-1/  and paste it in the Android studio inside kotlin data class file from JSON

(If the extension is not installed inside your android studio then go to File>Settings>Plugins>Search for JSON to Kotlin class and install the extension)

Format the copied data>Give class Name>Generate the data class


STEP 4 = Creating the API Interface

Create a new Kotlin Interface in your main Java Package and name it as ApiInterface 



```http
interface ApiInterface {

    @Headers("X-RapidAPI-Key:6b5dfcce33msh06e06ec4af4f8b2p18a89ejsndad351702d1d",
            "X-RapidAPI-Host:deezerdevs-deezer.p.rapidapi.com")
    @GET("search")
    fun getData(@Query("q")query: String): Call<MyData>
}

```

Now we will be writing retrofit Builder
go to your mainActivity.kt

```http



```











