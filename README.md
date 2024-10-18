
---

# Production Simulation

This project simulates a production process using Python classes. The simulation involves multiple production units that manufacture and transport products while maintaining inventory records.

## Features
- **Unit Class**: Represents a production unit with methods for manufacturing, transporting, and reporting inventory.
- **Simulation Function**: Simulates the production process over multiple cycles with customizable production and transportation values.

## Installation
Ensure you have Python installed on your machine. You can download it from [Python's official website](https://www.python.org/downloads/).

### Required Packages
No additional packages are required for this project, as it uses only built-in Python libraries.

## Usage
1. **Define Units**: Create instances of the `Unit` class for each production unit.
2. **Set Relationships**: Define upstream and downstream relationships between the units.
3. **Run the Simulation**: Call the `simulate_production_process` function with defined units, number of cycles, and production/transportation values.

### Example

```python
# Create units
unitA = Unit("A", "C1")
unitB = Unit("B", "C2")
unitC = Unit("C", "C3")
unitD = Unit("D", "C3")

# Set downstream and upstream relationships
unitA.set_downstream(unitC)
unitB.set_downstream(unitC)
unitC.add_upstream(unitB)
unitD.add_upstream(unitC)

# Run the simulation
x_values, y_values = simulate_production_process(units, num_cycles, production_values, transportation_values)
```

## License
This project is licensed under the MIT License. A product of **Gathu**

---
*This project was developed while sipping coffee and questioning whether I’m better at debugging code or making questionable life choices*
