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
The dataset provides information about 67 neighbourhoods in the LA region. Its content is relevant for anyone interested into understanding if a specific district is relevant for their needs. The following variables are presented:
* Name: For each row, it contains the name of the neighbourhood.
* Education Ranking: From 1 to 9 ranking the level of public school education, 1 being the worst and 9 the best.
* Safety Ranking: From 1 to 5, represented the level of neighbourhood safety, being 1 the worst and 5 the best.
* Average House Price: The estimated average housing price.

This dataset was manully constructed by our group taking Google Maps as a source.

# Usage
The user starts by entering their address, including the city and postcode, into the system. The system uses the Nominatim API to convert the entered address into geographical coordinates. The user is then prompted to enter the name of the medicine they are looking for. The PharmacyTree class processes the user input and searches its network of pharmacies to find those that have the specified medicine in stock. For each pharmacy that has the medicine, the system calculates the distance from the user's location using the Haversine formula. The system displays a list of pharmacies where the medicine is available, along with the distance to each pharmacy from the user's location. The system identifies the closest pharmacy with the required medicine and displays its name and distance. The address of the closest pharmacy is then provided to the user. If the address is not available in the system, a relevant message is displayed. The user can then decide to visit the pharmacy based on the information provided.

# Further Improvements
1. Implement Real-Time Inventory Updates: Enhance the inventory management system to reflect real-time changes in stock levels. This could involve integrating with pharmacy management systems for automatic updates.
2. Optimize Nearest Pharmacy Search: The current method _find_nearest_pharmacies is a placeholder. Implement an efficient algorithm to find the nearest pharmacies based on the user's location, possibly using geospatial data structures or services.
3. User Authentication and Profiles: Implement user authentication to manage personal information securely. User profiles could store medical history, preferences, and recurring prescriptions for a personalized experience.
4. Error Handling and Data Validation: Improve error handling for external API calls (e.g., Nominatim API) and validate data inputs to prevent incorrect or malicious data entries.
5. Interface with Healthcare Providers: Develop a system for healthcare providers to input prescriptions directly into the system, ensuring accuracy and reducing manual entry by users.
6. Expand the Pharmacy Network: Increase the number of pharmacies in the network, including those in rural or underserved areas.
7. Integration with Delivery Services: Implement a feature for home delivery of medicines, particularly useful for users with mobility issues or in times of public health emergencies.
8. Data Security and Privacy Compliance: Ensure the system is compliant with data protection regulations (like GDPR or HIPAA), especially since it handles sensitive health information.
9. Pharmacy Rating System: Introduce a rating system for pharmacies based on user experiences, which could help others make informed choices.
10. Analytics Dashboard: Develop an analytics dashboard for pharmacies to track demand trends, popular medicines, and user feedback, aiding in better inventory management.

Limitations:
1. Scalability: The tree structure for storing pharmacy data may not scale efficiently for a large number of pharmacies, especially when performing operations like searching for the nearest pharmacy.
2. Updating Pharmacy Inventory: There is no mechanism for real-time updates or synchronization of pharmacy inventories, which can lead to outdated information being presented to the user.
3. User Experience: The current command-line interface may not be as user-friendly as a graphical user interface, which could limit the accessibility of the application to a broader user base.
4. Error and Exception Handling: The script could be improved with more comprehensive error and exception handling to manage and respond to unexpected situations more gracefully.
5. Nearest Pharmacy Logic: The method _find_nearest_pharmacies is currently a placeholder and doesn't implement an actual nearest pharmacy finding algorithm. Implementing this feature effectively requires more sophisticated algorithms, potentially involving spatial data structures or geographic information system (GIS) techniques.

# Credits
The authors of this project are:
Yasmin Tandon
Leopoldo Sirolli
Juancho Mulato
Matías Viguera
Jean Carlos
