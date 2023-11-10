JiaoziDB is a version built database for machine learning. Instead of versioning files, JiaoziDB versions tables.

# Why schema?

Schemas improve data quality.

Data in the Machine Learning space is usually loosely structured, stored in CSVs or JSON. Schemas provide more information about the form and function of the data being stored, allowing for stricter constraints on data being used. Stricter constraints improve data quality by detecting bad data before it makes it into the database.

Text data used in NLP fits naturally in a relational database model unlike image and video data common in other Machine Learning verticals.

+ NLP
+ Medical Research & drug discovery
+ Configuration Management
+ Worldwide data collaboration to effectively work together on a shared biological model.
+ Version asset data in game development: For some games, it's appropriate to store asset data in database tables