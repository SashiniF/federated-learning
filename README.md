# Federated Airport System

## Overview
This is a Python project that simulates a Federated Airport System. The system allows for managing multiple airports, each containing flights with passengers and their baggage. The project demonstrates the relationship between flights, passengers, baggage, and airports.

## Features
- **Flight Management**: Each flight has an associated flight number, airline, destination, departure time, list of passengers, and baggage information.
- **Airport Management**: Multiple airports can be managed within the system, each containing multiple flights.
- **Federated System**: Airports can be added to a federated system that allows you to display information across all airports within the system.

## Project Structure
The project contains three main classes:
- **Flight**: Manages individual flight details, including passengers and baggage.
- **Airport**: Manages flights within an airport.
- **FederatedAirportSystem**: Manages multiple airports, displaying all flights within the federated system.

## Getting Started

### Prerequisites
- Python 3.x

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/federated-airport-system.git
   ```
2. Navigate to the project directory:
   ```bash
   cd federated-airport-system
   ```

### Running the Project
You can run the example code by executing:
```bash
python main.py
```

### Example Usage
Here is a sample flow that you can find in the `main.py`:

```python
airport1 = Airport("Airport 1")
flight1 = Flight("ABC123", "Airline A", "New York", "10:00")
flight1.add_passenger("John Smith")
flight1.add_baggage("John Smith", 20)
flight1.add_passenger("Alice Johnson")
flight1.add_baggage("Alice Johnson", 15)
airport1.add_flight(flight1)

airport2 = Airport("Airport 2")
flight2 = Flight("DEF789", "Airline B", "Los Angeles", "12:00")
flight2.add_passenger("Bob Brown")
flight2.add_baggage("Bob Brown", 18)
flight2.add_passenger("Eve Green")
flight2.add_baggage("Eve Green", 22)
airport2.add_flight(flight2)

federated_system = FederatedAirportSystem()
federated_system.add_airport(airport1)
federated_system.add_airport(airport2)

federated_system.display_all_flights()
```

This script will output details of all flights in the system.

## Classes

### `Flight`
- **Attributes**:
  - `flight_number` (str): The flight number.
  - `airline` (str): The airline operating the flight.
  - `destination` (str): The flight destination.
  - `departure_time` (str): The scheduled departure time.
  - `passengers` (list): A list of passengers on the flight.
  - `baggage` (dict): A dictionary of baggage weights for each passenger.

- **Methods**:
  - `add_passenger(passenger)`: Adds a passenger to the flight.
  - `add_baggage(passenger_name, baggage_weight)`: Adds baggage weight for a passenger.
  - `display_details()`: Displays all flight details including passengers and baggage.

### `Airport`
- **Attributes**:
  - `name` (str): The name of the airport.
  - `flights` (list): A list of flights managed by the airport.

- **Methods**:
  - `add_flight(flight)`: Adds a flight to the airport.
  - `display_flights()`: Displays details of all flights at the airport.

### `FederatedAirportSystem`
- **Attributes**:
  - `airports` (dict): A dictionary of airports managed within the federated system.

- **Methods**:
  - `add_airport(airport)`: Adds an airport to the federated system.
  - `display_all_flights()`: Displays all flights across all airports in the system.

