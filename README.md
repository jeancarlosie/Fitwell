# Fitwell
The all-in-one wellness platform.

Our platform has 2 primary functions:
* To verify the availability of medicines specified by the user in pharmacies near them.
* To deliver medicines to users.

Complex data structures and algorithms will be required to perform these functions, including trees, dictionaries, tree traversal, and search algorithm.

Watch the following video for more information: https://www.youtube.com/watch?v=NnMCcCeiTJ0

# Installation
To run our program, you must install:
* Python programming language (all version between 3.6 and 3.11).
* Python libraries: requests, maths. To install these libraries, type the following commands:
  * import requests
  * import maths
 
Now that you have installed all the requirements, open the file "Fitwell.py" and run the program.

# The Dataset
The dataset provides information on all 23 pharmacies in Segovia - Pharmacy name, street name, postal code. We constructed it manually in Excel using Google Maps as our source.

# Usage
The user starts by entering their address, including their city and postcode, into the system. The system uses the Nominatim API to convert the entered address into geographical coordinates. The user is then prompted to enter the name of the medicine they need to refill. The PharmacyTree class processes the medicine inputted and searches its network of pharmacies to find those that have the specified medicine in stock. For each pharmacy that currently carries the medicine, the system calculates the distance from the user's location using the Haversine formula. The system displays a list of pharmacies where the medicine is available, along with the distance to each pharmacy from the user's location. The system identifies the closest pharmacy carrying the medicine and displays its name, distance, and address. If the address is not available in the system, "Address not found for the closest pharmacy" is displayed. The user can then decide to visit the pharmacy based on the information provided.

Limitations:
1. Scalability: The tree structure for storing pharmacy data will be highly inefficient when the number of pharmacies is high, especially when performing operations such as searching for the nearest pharmacy, which has a running time of O(n).
2. Updating Pharmacy Inventory: There is no mechanism for real-time updates or synchronization of pharmacy inventories, which can lead to outdated information being presented to the user.

# Further Improvements
1. Implement Real-Time Inventory Updates: By integrating our system with pharmacy management systems, the inventory management system will reflect real-time changes in stock levels.
2. User Authentication: Implement user authentication to manage personal information securely, especially since health information is highly sensitive and confidential.
3. Interface with Healthcare Providers: Develop a system for healthcare providers to input their patients' prescriptions directly into the system, ensuring accuracy and reducing manual
   entry by users.
4. Integration with Delivery Services: Implement a feature that delivers medicines to the doorsteps of users in order to increase the accessibility of medicines for everyone, especially for people with limited mobility.
5. Analytics Dashboard: Develop an analytics dashboard for pharmacies to track demand trends for medicines, improving inventory management.

# Credits
The authors of this project are:
Yasmin Tandon
Leopoldo Sirolli
Juancho Mulato
Matías Viguera
Jean Carlos
