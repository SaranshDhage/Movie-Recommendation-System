# Movie Recommendation System

## Overview
This Django web application provides movie recommendations based on user preferences. It utilizes a custom algorithm to suggest movies that match the user's taste, enhancing their viewing experience.

## Features
- **User-Friendly Interface**: Simple and intuitive design for easy navigation.
- **Search Functionality**: Users can search for movies using keywords.
- **Recommendations**: The system suggests movies based on user preferences and viewing history.
- **Responsive Design**: Compatible with various devices and screen sizes.

## Technology Stack
- **Backend**: Django
- **Frontend**: HTML, CSS (Tailwind CSS), JavaScript (jQuery)
- **Database**: PostgreSQL (recommended for production)

## 1. Requirements:

To build this project without any errors/issues, the following requirements needs to be satisfied

1. Create a Virtual Environment using python>=3.8 (Tested on 3.9.16)

2. Install the dependencies from the requirements text file from the repository.

<hr>

## 2. Project Guide

#### 2.1 Running in Local

```shell
/path/to/env/bin/activate
```

Once done, you should go to project root directory and run the following command

```shell
python manage.py runserver
```

It will take a moment and then show the following output on the terminal.

<img title="" src="./readme_images/runserver_demo.png" alt="">

You can now open your browser and hit the server IP `http://localhost:8000` provided to run the demo on your local system. 

By default, this project will run on Demo model. If you wish to change model, you can train and download the model of your choice using the python notebook to get better or faster recommendations. Once trained, you can integrate by modifying these 2 lines of code inside `recommender/views.py`

```python
Line 5 : movies_data = pd.read_parquet("static/<dataset_name>.parquet")
Line 73: model = pa.parquet.read_table('static/<model_name>.parquet').to_pandas()
```

Note that you have to place dataset and model into the `static` directory.


This code implements a movie recommendation system based on user input. The system provides a simple web interface built on HTML, CSS, and JavaScript libraries. 

Inputs: The user can search for movies by providing a partial or complete movie name. 

Outputs: The system provides movie recommendations based on user input. 

Usage:

1. Open the HTML file in a web browser.
2. Type the name of a movie in the search bar, and the system will provide the movie recommendation. 

Note: Only the top 2.5K movies based on IMBD are present in this system's database.
