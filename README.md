# VOIS_AICTE_Oct2025_EerlaVarsha
A data visualization project on AirBNB hotel booking analysis

// BOOKINGS BY CITY
import pandas as pd
import matplotlib.pyplot as plt

# -------------------------------
# Step 1: Load or create dataset
# -------------------------------
# Example dataset (replace this with your Airbnb dataset CSV if available)
data = {
    "City": ["New York", "London", "Paris", "Tokyo", "Sydney",
             "New York", "London", "Paris", "Tokyo", "New York",
             "Sydney", "London", "Paris", "Tokyo", "Sydney"]
}

# Create DataFrame
df = pd.DataFrame(data)

# -------------------------------
# Step 2: Count bookings by city
# -------------------------------
city_counts = df["City"].value_counts()

# -------------------------------
# Step 3: Plot the chart
# -------------------------------
plt.figure(figsize=(7,5))
city_counts.plot(kind="bar", color="skyblue", edgecolor="black")

# Add labels and title
plt.title("Bookings by City", fontsize=14, fontweight="bold")
plt.xlabel("City", fontsize=12)
plt.ylabel("Number of Bookings", fontsize=12)
plt.xticks(rotation=45)
plt.grid(axis="y", linestyle="--", alpha=0.7)

# Save chart as image
plt.tight_layout()
plt.savefig("bookings_by_city.png", dpi=300)

# Show chart
plt.show()




// SEASONAL BOOKING TRENDS
# Import libraries
import pandas as pd
import matplotlib.pyplot as plt

# Sample data: Bookings by city
data = {
    'City': ['New York', 'Los Angeles', 'Chicago', 'Miami', 'San Francisco'],
    'Bookings': [120, 95, 75, 60, 80]
}

# Create a DataFrame
df = pd.DataFrame(data)

# Plot a bar chart
plt.figure(figsize=(10,6))
plt.bar(df['City'], df['Bookings'], color='skyblue')
plt.title('Airbnb Bookings by City', fontsize=16)
plt.xlabel('City', fontsize=12)
plt.ylabel('Number of Bookings', fontsize=12)
plt.xticks(rotation=45)
plt.grid(axis='y', linestyle='--', alpha=0.7)

# Show the chart
plt.tight_layout()
plt.show()

// BOOKING STATUS (confirmed vs cancellation)
