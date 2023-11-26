# Fitwell
The all-in-one wellness platform.

Our platform has 2 primary functions:
* To verify the availability of medicines specified by the user in pharmacies near them.
* To deliver medicines to users.

Complex algorithms will be required to perform these functions, including .

Watch the following video for more information: https://www.youtube.com/watch?v=NnMCcCeiTJ0

# Installation
To run our program, you must have the following things installed:
* Python programming language (all version between 3.6 and 3.11).
* Python libraries: requests, maths. To install these libraries, type the following commands:
  * import requests
  * import maths
 
Now that you have installed all the requirement, open the file "Fitwell.py" and run the program.

# Usage
The code you've shared is an example of a Python script designed to manage a network of pharmacies, track their inventories, and help users find nearby pharmacies that stock specific medicines. Let's break down its key components:

Classes
PharmacyNode: Represents a single pharmacy. It stores the pharmacy's name, location, inventory, and its child pharmacies (if any).

PharmacyTree: Manages a network of pharmacies. It holds a root node (the starting point of the network) and provides methods to add new pharmacies, find pharmacies stocking a specific medicine, and internal methods for tree navigation and pharmacy retrieval.

Functions
address_to_coordinates(address): Converts a textual address into geographical coordinates using the Nominatim API. This is used to find the user's location.

calculate_distance(coord1, coord2): Calculates the distance between two sets of coordinates using the Haversine formula. This is used to determine the nearest pharmacy to the user.

Script Flow
Initializes a PharmacyTree.
Adds pharmacies to the network with specified stocks.
Asks the user for an address and a medicine they are looking for.
Converts the address to coordinates.
Searches the pharmacy network for pharmacies that have the requested medicine in stock.
Determines the closest pharmacy with the medicine and provides its distance and address.
Key Concepts and Libraries
Object-Oriented Programming: The use of classes (PharmacyNode and PharmacyTree) to model real-world entities and their relationships.
Tree Data Structure: The pharmacies are organized in a tree structure, where each node can have multiple child nodes (representing child pharmacies).
Geolocation and Distance Calculation: Integration with an external geolocation service (Nominatim API) and implementation of the Haversine formula for distance calculation.
requests Library: Used for making HTTP requests to the Nominatim API.
math Library: Provides mathematical functions, used here for calculations in the Haversine formula.
Improvements or Considerations
The _find_nearest_pharmacies method currently returns all pharmacies, regardless of distance. This could be enhanced to actually find the nearest pharmacies based on geographical distance.
Error handling could be improved, especially for API requests and user inputs.
The script assumes a specific structure and relationships among pharmacies which might not always hold true in real-world scenarios. Adaptation to more complex or different hierarchical structures might be needed.

# Credits
The authors of this project are:
Yasmin Tandon
Leopoldo Sirolli
Juancho Mulato
Matías Viguera
Jean Carlos
