🌀 Spiral Web Art Generator
simple Python script that uses numpy and matplotlib to generate a geometric spiral pattern
This script plots a tight spiral and overlays it with a series of radial lines, creating a clean, striking visual

📋 Requirements
i)  numpy
ii) matplotlib

pip install numpy matplotlib

📜 The Code
import matplotlib.pyplot as plt
import numpy as np

# --- Parameters ---
# Feel free to change these values to see what happens!
num_lines = 50     # Number of radial lines from the center
num_turns = 10     # How many times the spiral winds around
num_points = 1000  # The smoothness/resolution of the spiral
# --- End of Parameters ---

# Set up the plot
fig, ax = plt.subplots(figsize=(6, 6))

# 1. Create the Spiral
# Create arrays for theta (angle) and r (radius)
theta = np.linspace(0, num_turns * 2 * np.pi, num_points)
r = np.linspace(0, 1, num_points)

# Convert from polar (r, theta) to cartesian (x, y) coordinates
x = r * np.cos(theta)
y = r * np.sin(theta)

# Plot the spiral
ax.plot(x, y, color='black')

# 2. Create the Radial Lines ("Web")
for i in range(num_lines):
    # Calculate the angle for each line
    angle = 2 * np.pi * i / num_lines
    
    # Define the (x, y) start and end points for the line
    # All lines start at the origin (0, 0)
    x_line = [0, np.cos(angle)]
    y_line = [0, np.sin(angle)]
    
    # Plot the line
    ax.plot(x_line, y_line, color='black', linewidth=0.8)

# 3. Clean up and Display
ax.axis('off')  # Hide the X and Y axes
plt.show()      # Show the final artwork
