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




**Image Duplicate Scanner**
This script scans an API for duplicate images and stores information about them in a database table. The script uses a hashing algorithm to detect duplicate images, and can handle images in JPEG, PNG, and SVG formats.

Getting Started
To use this script, you'll need to install Python 3.x and the required dependencies listed in requirements.txt. You can install the dependencies by running:

Copy code
pip install -r requirements.txt
Once you have the dependencies installed, you can run the script with the following command:

css
Copy code
python scanner.py --api_url <API_URL> --database_file <DATABASE_FILE> --hash_algorithm <HASH_ALGORITHM>
Replace <API_URL> with the URL of the API to scan, <DATABASE_FILE> with the name of the database file to use, and <HASH_ALGORITHM> with the hashing algorithm to use (e.g. sha256).

Configuration
You can configure the script by modifying the following constants in scanner.py:

API_URL: The URL of the API to scan.
HASH_ALGORITHM: The hashing algorithm to use.
DUPLICATES_TABLE_NAME: The name of the database table to use for storing information about duplicate images.
DATABASE_FILE_NAME: The name of the database file to use.
You can also modify the detect_image_format() and convert_svg_to_png() functions to support additional image formats or to modify the SVG conversion process.

Database Schema
The script creates a database table called duplicates with the following schema:

Column	Type	Description
token	TEXT	The hash value of the image data.
info	TEXT	The response data from the API for the image.
timestamp	TEXT	The timestamp when the image was detected as a duplicate.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
This script was inspired by this Stack Overflow answer and uses the following third-party libraries:

requests for making HTTP requests.
Pillow for image manipulation.
xml.etree.ElementTree for parsing SVG images.
CairoSVG for converting SVG images to PNG.
