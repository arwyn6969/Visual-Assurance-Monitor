Image Scanner and Database Updater
A Python script that scans images from an API feed and extracts relevant data using OCR and regular expressions. The extracted data is stored in a SQLite database for later use. The script includes error handling, logging, and other features to ensure robustness and reliability.

Requirements
Python 3.x
requests
pytesseract
Pillow
SQLite3
Installation
Clone the repository to your local machine.
Install the required Python libraries using pip install -r requirements.txt.
Run the script using python scanner.py.
Usage
Set the api_url variable to the URL of the API that provides the images to scan.
Modify the regular expression pattern in the pattern variable to match the fields you want to extract from the images.
Run the script and wait for it to finish scanning the images and updating the database.
Database
The extracted data is stored in a SQLite database named mydb.db. The database includes a table named mytable with columns for the extracted fields (p, op, tick, amt, and limit).

Error Handling
The script includes error handling to catch and log any exceptions that might occur during its execution. If an error occurs, the script exits with a non-zero exit code.

Logging
The script uses the Python logging module to write log messages to a file named scanner.log. The log file includes timestamps, log levels, and log messages.

License
This project is licensed under the MIT License. You are free to use, modify, and distribute this code as you see fit.

Contributing
Contributions to this project are welcome. If you find a bug or have a feature request, please open an issue or submit a pull request.

Acknowledgments
The pytesseract library used in this project is based on the Tesseract OCR engine, developed by Google.
The requests library used in this project is developed and maintained by Kenneth Reitz and contributors.
This README file provides clear instructions on how to install and use the tool, along with information on the database, error handling, and logging. It also includes licensing information and guidelines for contributing to the project.
