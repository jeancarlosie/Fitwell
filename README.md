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

# Data

# Usage
The user starts by entering their address, including their city and postcode, into the system. The system uses the Nominatim API to convert the entered address into geographical coordinates. The user is then prompted to enter the name of the medicine they need to refill. The PharmacyTree class processes the medicine inputted and searches its network of pharmacies to find those that have the specified medicine in stock. For each pharmacy that currently carries the medicine, the system calculates the distance from the user's location using the Haversine formula. The system displays a list of pharmacies where the medicine is available, along with the distance to each pharmacy from the user's location. The system identifies the closest pharmacy carrying the medicine and displays its name, distance, and address. If the address is not available in the system, "Address not found for the closest pharmacy" is displayed. The user can then decide to visit the pharmacy based on the information provided.

We have also written another code that enables pharmacies to input and update their stock levels in the system, allowing for real-time updates and synchronisation of pharmacy inventories - all information presented to the user is accurate.

Limitations:
1. Scalability: The tree structure for storing pharmacy data will be highly inefficient when the number of pharmacies is high, especially when performing operations such as searching for the nearest pharmacy, which has a running time of O(n).

# Further Improvements
1. User Authentication: Implement user authentication to manage highly sensitively and confidential health information.
2. Interface with Healthcare Providers: Develop a system for healthcare providers to input their patients' prescriptions directly into the system, ensuring they are taking the right medicines in the right doses and reducing manual entry by users.
3. Integration with Delivery Services: Implement a feature that delivers medicines to the doorsteps of users in order to increase the accessibility of medicines for everyone, especially for people with limited mobility.
4. Analytics Dashboard: Develop an analytics dashboard for pharmacies to track demand trends for medicines over time, improving inventory management.

# Credits
The authors of this project are:
Yasmin Tandon
Leopoldo Sirolli
Juancho Mulato
Matías Viguera
Jean Carlos
