# masters portfolio programs
# File: data_analysis.py
import pandas as pd
import matplotlib.pyplot as plt

# Generate synthetic data
data = {
    "Month": ["Jan", "Feb", "Mar", "Apr", "May"],
    "Revenue": [15000, 22000, 18000, 25000, 20000],
    "Expenses": [10000, 12000, 15000, 18000, 12000],
}

# Create DataFrame
df = pd.DataFrame(data)

# Data Analysis
total_revenue = df["Revenue"].sum()
average_expenses = df["Expenses"].mean()

print(f"Total Revenue: ${total_revenue}")
print(f"Average Expenses: ${average_expenses}")

# Data Visualization
plt.plot(df["Month"], df["Revenue"], label="Revenue")
plt.plot(df["Month"], df["Expenses"], label="Expenses")
plt.xlabel("Month")
plt.ylabel("Amount ($)")
plt.title("Revenue and Expenses Over Months")
plt.legend()
plt.show()
