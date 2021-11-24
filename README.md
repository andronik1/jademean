# Mean calculation with JADE

### Algorithm

Every agent sends each other all the info it knows. Then every agents is waiting for the messages from the other agents. This continues until all the information is received by every agent. Mean value is calculated by each agent independently.

### Estimation

Memory: `O(n*n)`
Messages: `O(n*n)`
Messages to the center: `0`
Ticks: `O(n)`

### How to build

* Create the `lib` directory in the root of the project
* Put the JADE library jar-file into it
* Run with `gradlew`

### Example output
