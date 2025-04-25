Movie Recommendation System (MRS)
This repository contains all the project files and necessary details about applications required to run the project on your local machine as well as host it as a Django Application on your Server/Domain.

Title	Description	Link
Demo :movie_camera:	Sample Demo of MRS Hosted on free cloud PaaS	👇 Refer
Requirements :heavy_check_mark:	Requirements and essential links to get started with the project locally	👇 Refer
Model Training :small_red_triangle_down:	How the MRS was trained for Demo as well as on Large Movie Dataset from Kaggle	👇 Refer
Project Versatility :page_with_curl:	Reference documentation of how to plug in any general recommendation model into this project and host it on servers	👇Refer
Troubleshooting Issues :muscle:	Guide to resolve errors faced during reproducibility	To be Updated
Do you like it? ❤️ Follow me on Twitter, GitHub, & LinkedIn to say Hi 👋

1. Demo 🎥
In this section, we try to understand through video demo to play around the project and what all can be achieved through it.

Movie Recommendation System Hosted Application Demo

Running MRS on local System

Sample Screenshots

Home Screen

Home Screen
Navigation Screen

Navigation Screen
Search with Auto Suggestion

Search Functionality
Recommended Movies

Movie Recommended Results
Please be slightly patient while I create and upload the demo video. Follow and star this project to get latest notifications and update. 🙌

2. Requirements ✔️
To build this project without any errors/issues, the following requirements needs to be satisfied

Create a Virtual Environment using python>=3.8 (Tested on 3.9.16)

Install the dependencies from the requirements text file from the repository.

3. Model Training 🔻
3.1 Training & Inference
For complete guide to training your model and inference using the trained model, refer to "Movie Recommendation System Python Notebook".

3.2 Django Web Application Integration
Here is a detailed blog explaining about complete approach and directory structure essential to understand Django integration.

4. Project Guide
4.1 Running it OnRender Free Cloud
Here is a detailed blog explaining about complete approach and essential details to deploy not just this application but also any other web-application you like to built.

4.2 Running in Local
I am assuming you have completed section 2 in the above reference for creating your environment. Let's start by activating it.

/path/to/env/bin/activate
Once done, you should go to project root directory and run the following command

python manage.py runserver
It will take a moment and then show the following output on the terminal.



You can now open your browser and hit the server IP http://localhost:8000 provided to run the demo on your local system.

By default, this project will run on Demo model. If you wish to change model, you can train and download the model of your choice using the python notebook to get better or faster recommendations. Once trained, you can integrate by modifying these 2 lines of code inside recommender/views.py

Line 5 : movies_data = pd.read_parquet("static/<dataset_name>.parquet")
Line 73: model = pa.parquet.read_table('static/<model_name>.parquet').to_pandas()
Note that you have to place dataset and model into the static directory.

This code implements a movie recommendation system based on user input. The system provides a simple web interface built on HTML, CSS, and JavaScript libraries.

Inputs: The user can search for movies by providing a partial or complete movie name.

Outputs: The system provides movie recommendations based on user input.

Dependencies:

static/recommender/ -- contains the following CSS files: cursor.css, page.css, and navbar.css
static/logo.png -- the logo of the application
static/production ID_4779866.mp4 -- a background video for the web page
@tabler/icons@latest/iconfont/tabler-icons.min.css
normalize/5.0.0/normalize.min.css
jquery-ui.css
font-awesome.min.css
bootstrap.min.css
jquery.min.js
jquery-ui.js
Usage:

Open the HTML file in a web browser.
Type the name of a movie in the search bar, and the system will provide the movie recommendation.
