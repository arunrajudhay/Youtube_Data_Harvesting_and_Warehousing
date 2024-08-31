# Youtube_Data_Harvesting_and_Warehousing 
## Introduction 
YouTube Data Harvesting and Warehousing is a project aimed at developing a user-friendly Streamlit application that leverages the power of the Google API to extract valuable information from YouTube channels. The extracted data is then stored in a SQL data warehouse, and made accessible for analysis and exploration within the Streamlit app.
Table of Contents

## Table of Contents
1. Pre-requisites
2. Key Technologies and Skills
3. Usage
4. Data Scrapping
5. Storing in MySQL
6. Querying
7. Viewing and Visualization
8. Further Improvements

## Pre-requisites :
Install the following packages to run the project :
1. pip install streamlit
2. pip install google-api-python-client
3. pip install mysql-connector-python
4. pip install pandas
5. pip install plotly-express
6. pip install streamlit_option_menu

## Key Technologies and Skills
1. Python scripting
2. Web scraping
3. MYSQL querying
4. Application Programming Interface (API) integration
5. Streamlit development
6. Plotly visualization

## Usage
To use this project, follow these steps:
1. Clone the repository
2. Install the required packages
3. Run the Streamlit app
4. Access the app in your browser

## Data Scrapping
The project uses Google API key to connect with youtube API and fetch the all details about the channel, given the channel ID. Further the data scrapped is presented in JSON format to users of the streamit application.

## Storing in MYSQL
Connecting python with MYSQL using mysql.connector allows us to store data in a structured format. Initally, we prepare the data by extracting the required features in channel, video and comments section of the JSON document. Later, we perform a query to check if the channel scrapped already exists in our database or not. If it is avaiable, we are going to update the document with the specified channelID. Else, we insert the channel information as a new document into MYSQL.We have already created 4 tables in the backend called channel, video and comment. The tables have been described below.

Table : Channel
| Column Name         | Data Type       | Description                        |
|---------------------|-----------------|------------------------------------|
| `channel_id`        | `VARCHAR(255)`  | Unique identifier of the channel   |
| `channel_name`      | `VARCHAR(255)`  | Name of the channel                |
| `views_count`       | `INT`           | Total views for the channel        |
| `description`       | `TEXT`          | Description of the channel         |
| `subscription_count`  | `INT`         | Total channel subscribers          |

Table : Video
| Column Name        | Data Type      | Description                                          |
|--------------------|----------------|------------------------------------------------------|
| `video_id`         | `VARCHAR(255)` | Unique identifier of the video                       |
| `video_name`       | `VARCHAR(255)` | Name of the video                                    |
| `channel_name`     | `VARCHAR(255)` | Name of the channel                                  |
| `video_description`| `VARCHAR(255)` | Description of the video                             |
| `published_at`     | `DATETIME`     | Date and time at which the video is published        |
| `view_count`       | `INT`          | Total views for the video                            |
| `like_count`       | `INT`          | Total likes for the video                            |
| `favorite_count`   | `INT`          | Total number of viewers who marked the video as favorite |
| `comment_count`    | `INT`          | Total comments for the video                         |
| `duration`         | `INT`          | Duration of the video in seconds                     |
| `thumbnail`        | `VARCHAR(255)` | Link to the thumbnail image                          |
| `caption_status`   | `VARCHAR(255)` | Caption status of the video                          |

Table : Comment
| Column Name           | Data Type      | Description                                 |
|-----------------------|----------------|---------------------------------------------|
| `comment_id`          | `VARCHAR(255)` | Unique identifier of the comment            |
| `comment_text`        | `TEXT`         | Text content of the comment                 |
| `comment_author`      | `VARCHAR(255)` | Name or identifier of the comment's author  |
| `comment_published_at`| `DATETIME`     | Date and time at which the comment was published |

Table : Playlist
| Column Name  | Data Type      | Description                          |
|--------------|----------------|--------------------------------------|
| `playlist_id`| `VARCHAR(255)` | Unique identifier of the playlist    |
| `channel_id` | `VARCHAR(255)` | Unique identifier of the channel     |
| `playlist_name` | `VARCHAR(255)` | Name of the playlist                |

## Querying
There exists 10 pre-defined queries in "Query" tab of the portal. Choosing any one from the select box allows us to query the tables accordingly.

## Viewing and Visualizing
We can view the 4 tables (channel, video, comment and playlist) present in SQL in the streamlit application by Navigating to the "View" tab.
Also, streamlit visualization functions help us understand the power of visualization by plotting scatter plots, bar charts and line graphs in the "Visualize" tab.

## Further Improvements
The project can further be enhanced by performing sentimental analysis on the video description and comments extracted for each video. This will help us to better understand and organize the genere of the video published, which in turn can be given as a recommendation for the preferred age group of viewers.
If you encounter any issues or have suggestions for improvements, feel free to reach out.

Email : [ruarunraj2013@gmail.com](mailto:ruarunraj2013@gmail.com)
Linkedin : [Arunraj Udayakumar's LinkedIn Profile](https://www.linkedin.com/in/arunraj-udayakumar-27722a146/)

