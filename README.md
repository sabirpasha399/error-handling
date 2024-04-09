# Geyser Smart Contract

This Solidity smart contract represents a simple Geyser that tracks temperature and water level. The contract allows setting the temperature and water level, with certain conditions and events triggered based on those values.

## Contract Details

### State Variables
- `temperature`: An unsigned integer representing the current temperature of the geyser.
- `waterLevel`: An unsigned integer representing the current water level of the geyser.

### Events
- `GeyserTurnedOff`: Triggered when the temperature surpasses a certain threshold, leading to the geyser turning off.
- `WaterLevelMaxCapacityReached`: Triggered when the water level reaches its maximum capacity.

### Functions
1. `setTemperature(uint256 _temperature)`: Sets the temperature of the geyser. It requires the temperature to be below a certain threshold to keep the geyser operational. If the temperature exceeds this threshold, the geyser will turn off, triggering the `GeyserTurnedOff` event.

2. `setWaterLevel(uint256 _waterLevel)`: Sets the water level of the geyser. It asserts that the water level is above a certain minimum threshold. If the water level reaches a specific maximum capacity, it reverts the transaction and triggers the `WaterLevelMaxCapacityReached` event.
