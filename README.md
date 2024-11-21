# Challenge Topic: Car Garage Management

**Problem Description**: You are tasked with managing a car garage that can hold a certain number of cars. Each car has a unique identifier (ID) and a status indicating whether it is currently parked in the garage or not. Your goal is to implement a simple system to manage the parking and unparking of cars in the garage.

**Function Signature**:
```typescript
class Garage {
    constructor(capacity: number);
    park(carId: string): boolean;
    unpark(carId: string): boolean;
    getParkedCars(): string[];
}
```

**Constraints**:
- The `Garage` class should be initialized with a `capacity` parameter, which is a positive integer representing the maximum number of cars that can be parked in the garage.
- The `park` method should take a `carId` (string) as input and return `true` if the car was successfully parked, or `false` if the garage is full or the car is already parked.
- The `unpark` method should take a `carId` (string) as input and return `true` if the car was successfully unparked, or `false` if the car was not found in the garage.
- The `getParkedCars` method should return an array of strings representing the IDs of all currently parked cars.

# Steps

1. Create a class `Garage` that maintains a list of parked cars and a maximum capacity.
2. Implement the `park` method to add a car to the garage if there is space available and the car is not already parked.
3. Implement the `unpark` method to remove a car from the garage if it is currently parked.
4. Implement the `getParkedCars` method to return the list of parked car IDs.

# Output Format

- The output of the `park` and `unpark` methods should be a boolean value (`true` or `false`).
- The output of the `getParkedCars` method should be an array of strings.

# Examples

**Example 1**  
```typescript
const garage = new Garage(2);
console.log(garage.park("CAR123")); // Output: true
console.log(garage.park("CAR456")); // Output: true
console.log(garage.park("CAR789")); // Output: false (garage is full)
console.log(garage.getParkedCars()); // Output: ["CAR123", "CAR456"]
console.log(garage.unpark("CAR123")); // Output: true
console.log(garage.getParkedCars()); // Output: ["CAR456"]
```

**Example 2**  
```typescript
const garage = new Garage(1);
console.log(garage.park("CAR001")); // Output: true
console.log(garage.park("CAR002")); // Output: false (garage is full)
console.log(garage.unpark("CAR003")); // Output: false (car not found)
console.log(garage.getParkedCars()); // Output: ["CAR001"]
```

# Notes

- Ensure that the `park` method checks for both capacity and whether the car is already parked.
- Ensure that the `unpark` method checks if the car is currently parked before attempting to remove it.
- The `getParkedCars` method should return the current state of parked cars at any point in time.