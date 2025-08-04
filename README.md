MyRecommendationSystem

A simple User-Based Collaborative Filtering recommendation system using Apache Mahout. This Java project reads user-item rating data from a CSV file and generates recommendations based on similar users' preferences.


Features:

- User-based collaborative filtering
- Pearson correlation similarity
- Top-N user neighborhood (NearestNUserNeighborhood)
- Reads input from a CSV file
- Uses Apache Mahout for recommendation engine

Features: 

- User-based collaborative filtering  
- Pearson correlation similarity  
- Top-N user neighborhood (NearestNUserNeighborhood)  
- Reads input from a CSV file  
- Uses Apache Mahout for recommendation engine  

Project Structure:

MyRecommendationSystem/
│
├── src/
│ ├── SampleData.csv # Dataset (userID,itemID,preference)
│ └── com/mycompany/myrecommendationsystem/
│ └── MyRecommendationSystem.java # Main Java class
├── pom.xml # Maven configuration


How It Works:

1. Reads a CSV file containing user preferences.
2. Calculates similarity between users using Pearson Correlation.
3. Selects the nearest N users (neighbors).
4. Recommends items liked by similar users but not yet consumed by the target user.

Sample CSV Format:


Make sure `SampleData.csv` exists at:  
`src/SampleData.csv`

Place `SampleData.csv` in `src/` like below:

1,101,4.0
1,102,3.5
2,101,4.5
2,103,2.0
3,102,2.5
3,103,4.0


How to Run:

Requirements:

- Java 8 (JDK 1.8)
- Apache Maven
- NetBeans or any IDE (IntelliJ, Eclipse)

Steps to Execute:

1. Clone or download this project.
2. Place your `SampleData.csv` in the `src/` directory.
3. Open terminal inside project root and run:
   ```bash
   mvn clean install
   mvn exec:java