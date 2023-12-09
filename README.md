# Fitwell
The all-in-one wellness platform.

Our platform has 2 primary functions:
* To verify the availability of medicines specified by the user in pharmacies in Segovia.
* To find the nearest pharmacy to the user with the desired medicine in stock.

Complex data structures and algorithms will be required to perform these functions, including trees, dictionaries, tree traversal, and search algorithm.

# File Architecture
* forPharmacy.py: Manages pharmacy and medicine data, inputted by pharmacies themselves.
* forUser.py: Manages user interactions, allowing them to search for the nearest pharamcies that have their desired medicine in stock.

# Dataset
The dataset includes the name, location, names of the medicines being sold at the pharmacy and their stock level, for each pharmacy in Segovia. This data will be manually inputted by each pharmacy using the program "forPharmacy", which will be written to a CSV file named "pharmacy_data.csv". This allows for real-time updates and synchronisation of pharmacy inventories.

# Requirements
We have written 2 codes, one for user use and one for pharmacy use. We have developed both codes in the macOS operating system.

The code for USER USE has been designed to run in a programming language where the following conditions have been met:
* Python environment (all versions between 3.6 and 3.11).
* Python libraries: requests, maths, csv. To install these libraries, type the following commands:
  * import requests
  * import maths
  * import csv
* Internet access: The Python environment will need access to the internet iin order to make HTTP requests to the Nominatim API, which will 
  convert the user's address to coordinates.
* File system access: The code needs to be run in an environment where it has permission to read and write to the file.
* User input: The code relies on user inputs, so it must be run in an environment that supports interactive user input, such as an
  interactive Python environment.

The code for PHARMACY USE has been designed to run in a programming language where the following conditions have been met:
* Python environment (all versions between 3.6 and 3.11).
* Python libraries: csv. To install this library, type the following commands:
  * import csv
* File system access: The code needs to be run in an environment where it has permission to read and write to the file.
* User input: The code relies on user inputs, so it must be run in an environment that supports interactive user input, such as an
  interactive Python environment.

Now that you have installed all the requirements, you can run the app.

# Usage
Assuming you have a an environment to run Python with, you must follow the following steps in order to install and run the app (assuming you have met all the requirements mentioned above).
1. Download the ZIP from the GitHub Repository.
2. Extract the ZIP file into a directory of your choice.
3. Run the "userUse" or/and "pharmacyUse" Python scripts, which should be in the extracted folder. Write:
  * python userUse.py
  * python pharmacyUse.py

# Usage for Code
The user starts by entering their address, including their city and postcode, into the system. The user is then asked to enter the name of the medicine they need to refill. The PharmacyTree class processes the medicine inputted and searches its network of pharmacies to find those that have the specified medicine in stock. For each pharmacy that currently carries the medicine, the system calculates the distance from the user's location. The system displays a list of pharmacies where the medicine is available, along with the distance to each pharmacy from the user's location. The system identifies the closest pharmacy carrying the medicine and displays its name, distance, and address. If the address is not available in the system, "Address not found for the closest pharmacy" is displayed. The user can then decide whether to visit the pharmacy based on the information provided.

We have also written another code that enables pharmacies to input and update their stock levels in the system, allowing for real-time updates and synchronisation of pharmacy inventories - all information presented to the user is accurate.

Limitations:
1. Scalability: The tree structure for storing pharmacy data will be highly inefficient when the number of pharmacies is high, especially when performing operations such as searching for the nearest pharmacy, which has a running time of O(n).

# User Stories
Prescription refill management:  User opens the app → Assuming that they have an activated account, the user clicks on the pill icon on the homepage → User’s prescribed drugs and their corresponding dosing schedules is displayed (both of which are inputted into the system by the user’s healthcare provider - this feature is only available to users with healthcare providers who have implemented Fitwell into the healthcare system) → User taps on the prescribed drug that they want to refill →If the user’s healthcare provider has authorized a prescription refill within the app, the user will be directed to a pharmacy inventory page displaying the nearest pharmacies carrying the prescribed drug - for each pharmacy that is displayed, the distance from the user’s current location to the pharmacy and the availability of the prescribed drug at the pharmacy will also be displayed. If the user’s healthcare provider has not authorized a prescription refill within the app, the interface will not respond.

Watch the following video for more information: https://www.youtube.com/watch?v=NnMCcCeiTJ0

# Further Improvements
1. User Authentication: Implement user authentication to manage highly sensitive and confidential health information.
2. Interface with Healthcare Providers: Develop a system for healthcare providers to input their patients' prescriptions directly into the system, ensuring they are taking the right medicines in the right doses and reducing manual entry by users.
3. Integration with Delivery Services: Implement a feature that delivers medicines to the doorsteps of users in order to increase the accessibility of medicines for everyone, especially for people with limited mobility.
4. Analytics Dashboard: Develop an analytics dashboard for pharmacies to track demand trends for medicines over time, improving inventory management.
5. Error handling: Error handling for user inputs to prevent issues from arising due to invalid or incomplete inputs.
6. Efficiency: Increase the efficiency of the program by using more efficient data structures and algorithms to manage the pharmacy data. We could use k-d trees or quadtrees instead of general tree structures to reduce the number of distance calculations neede and therefore reduce the running time of nearest neighbour search. 

# Credits
The authors of this project are:
Yasmin Tandon,
Leopoldo Sirolli, 
Juancho Mulato, 
Matías Viguera, 
Jean Carlos
