# Mean calculation with JADE

### Algorithm

Every agent sends each other all the info it knows. Then every agents is waiting for the messages from the other agents. This continues until all the information is received by every agent. Mean value is calculated by each agent independently. Also, Local Voting protocol is implemented.

### Estimation

Memory: `O(n*n)`
Messages: `O(n*n)`
Messages to the center: `0`
Ticks: `O(n)`

### How to build

* Create the `lib` directory in the root of the project
* Put the JADE library jar-file into it
* Run with `./gradlew run`

### Example output

```
INFO: --------------------------------------
Agent container Main-Container@172.17.0.1 is ready.
--------------------------------------------
Agent #1 with num = 13 and with neighbours: 7 10
Agent #1 sent 1 13;
Agent #2 with num = 17 and with neighbours: 3 5 7
Agent #2 sent 2 17;
Agent #4 with num = 9 and with neighbours: 7 10
Agent #3 with num = 11 and with neighbours: 2 8
Agent #3 sent 3 11;
Agent #4 sent 4 9;
Agent #3 got 2 17; from 2
Agent #3 sent 2 17;3 11;
Agent #2 got 3 11; from 3
Agent #2 got 2 17;3 11; from 3
Agent #2 sent 2 17;3 11;
Agent #5 with num = 3 and with neighbours: 2
Agent #5 sent 5 3;
Agent #2 got 5 3; from 5
Agent #2 sent 2 17;3 11;5 3;
Agent #3 got 2 17;3 11; from 2
Agent #3 got 2 17;3 11;5 3; from 2
Agent #8 with num = 5 and with neighbours: 3
Agent #7 with num = 14 and with neighbours: 1 2 4
Agent #7 sent 7 14;
Agent #6 with num = 7 and with neighbours: 9
Agent #6 sent 6 7;
Agent #8 sent 8 5;
Agent #1 got 7 14; from 7
Agent #1 sent 1 13;7 14;
Agent #3 sent 2 17;3 11;5 3;
Agent #2 got 2 17;3 11;5 3; from 3
Agent #8 got 2 17;3 11;5 3; from 3
Agent #8 sent 2 17;3 11;5 3;8 5;
Agent #2 got 7 14; from 7
Agent #2 sent 2 17;3 11;5 3;7 14;
Agent #5 got 2 17;3 11; from 2
Agent #5 got 2 17;3 11;5 3; from 2
Agent #7 got 1 13;7 14; from 1
Agent #5 sent 2 17;3 11;5 3;
Agent #7 sent 1 13;7 14;
Agent #3 got 8 5; from 8
Agent #3 sent 2 17;3 11;5 3;8 5;
Agent #4 got 7 14; from 7
Agent #4 sent 4 9;7 14;
Agent #4 got 1 13;7 14; from 7
Agent #4 sent 1 13;4 9;7 14;
Agent #2 got 2 17;3 11;5 3; from 5
Agent #1 got 1 13;7 14; from 7
Agent #2 got 1 13;7 14; from 7
Agent #2 got 2 17;3 11;5 3;8 5; from 3
Agent #2 sent 1 13;2 17;3 11;5 3;7 14;8 5;
Agent #8 got 2 17;3 11;5 3;8 5; from 3
Agent #2 sent 1 13;2 17;3 11;5 3;7 14;8 5;
Agent #10 with num = 16 and with neighbours: 1 9
Agent #5 got 2 17;3 11;5 3;7 14; from 2
Agent #10 sent 10 16;
Agent #3 got 2 17;3 11;5 3;8 5; from 8
Agent #7 got 2 17;3 11;5 3;7 14; from 2
Agent #5 sent 2 17;3 11;5 3;7 14;
Agent #7 got 4 9;7 14; from 4
Agent #3 got 2 17;3 11;5 3;7 14; from 2
Agent #7 sent 1 13;2 17;3 11;4 9;5 3;7 14;
Agent #10 got 4 9;7 14; from 4
Agent #7 sent 1 13;2 17;3 11;4 9;5 3;7 14;
Agent #10 sent 4 9;7 14;10 16;
Agent #9 with num = 3 and with neighbours: 6 10
Agent #9 sent 9 3;
Agent #3 sent 2 17;3 11;5 3;7 14;8 5;
Agent #9 got 6 7; from 6
Agent #9 sent 6 7;9 3;
Agent #10 got 1 13;4 9;7 14; from 4
Agent #10 sent 1 13;4 9;7 14;10 16;
Agent #4 got 1 13;2 17;3 11;4 9;5 3;7 14; from 7
Agent #6 got 9 3; from 9
Agent #6 sent 6 7;9 3;
Agent #4 sent 1 13;2 17;3 11;4 9;5 3;7 14;
Agent #10 got 9 3; from 9
Agent #10 sent 1 13;4 9;7 14;9 3;10 16;
Agent #6 got 6 7;9 3; from 9
Agent #10 got 6 7;9 3; from 9
Agent #10 sent 1 13;4 9;6 7;7 14;9 3;10 16;
Agent #10 got 1 13;2 17;3 11;4 9;5 3;7 14; from 4
Agent #10 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16;
Agent #1 got 10 16; from 10
Agent #2 got 2 17;3 11;5 3;7 14; from 5
Agent #1 got 1 13;2 17;3 11;4 9;5 3;7 14; from 7
Agent #2 got 1 13;2 17;3 11;4 9;5 3;7 14; from 7
Agent #1 sent 1 13;2 17;3 11;4 9;5 3;7 14;10 16;
Agent #2 got 1 13;2 17;3 11;4 9;5 3;7 14; from 7
Agent #4 got 1 13;2 17;3 11;4 9;5 3;7 14; from 7
Agent #2 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;
Agent #1 sent 1 13;2 17;3 11;4 9;5 3;7 14;10 16;
Agent #1 got 1 13;2 17;3 11;4 9;5 3;7 14; from 7
Agent #2 got 2 17;3 11;5 3;7 14;8 5; from 3
Agent #1 got 4 9;7 14;10 16; from 10
Agent #1 got 1 13;4 9;7 14;10 16; from 10
Agent #8 got 2 17;3 11;5 3;7 14;8 5; from 3
Agent #1 got 1 13;4 9;7 14;9 3;10 16; from 10
Agent #1 got 1 13;4 9;6 7;7 14;9 3;10 16; from 10
Agent #8 sent 2 17;3 11;5 3;7 14;8 5;
Agent #10 got 1 13;2 17;3 11;4 9;5 3;7 14;10 16; from 1
Agent #1 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16;
Agent #10 got 1 13;2 17;3 11;4 9;5 3;7 14;10 16; from 1
Agent #10 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 1
Agent #3 got 1 13;2 17;3 11;5 3;7 14;8 5; from 2
Agent #1 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16;
Agent #1 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 10
Agent #3 got 1 13;2 17;3 11;5 3;7 14;8 5; from 2
Agent #3 sent 1 13;2 17;3 11;5 3;7 14;8 5;
Agent #10 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 1
Agent #2 got 1 13;2 17;3 11;5 3;7 14;8 5; from 3
Agent #8 got 1 13;2 17;3 11;5 3;7 14;8 5; from 3
Agent #3 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 2
Agent #8 sent 1 13;2 17;3 11;5 3;7 14;8 5;
Agent #3 got 2 17;3 11;5 3;7 14;8 5; from 8
Agent #9 got 10 16; from 10
Agent #3 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;
Agent #9 got 4 9;7 14;10 16; from 10
Agent #8 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 3
Agent #2 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 3
Agent #3 got 1 13;2 17;3 11;5 3;7 14;8 5; from 8
Agent #8 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;
Agent #9 sent 4 9;6 7;7 14;9 3;10 16;
Agent #3 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 8
Agent #6 got 4 9;6 7;7 14;9 3;10 16; from 9
Agent #9 sent 4 9;6 7;7 14;9 3;10 16;
Agent #6 sent 4 9;6 7;7 14;9 3;10 16;
Agent #10 got 4 9;6 7;7 14;9 3;10 16; from 9
Agent #6 got 4 9;6 7;7 14;9 3;10 16; from 9
Agent #9 got 1 13;4 9;7 14;10 16; from 10
Agent #9 got 6 7;9 3; from 6
Agent #10 got 4 9;6 7;7 14;9 3;10 16; from 9
Agent #5 got 1 13;2 17;3 11;5 3;7 14;8 5; from 2
Agent #9 sent 1 13;4 9;6 7;7 14;9 3;10 16;
Agent #9 got 1 13;4 9;7 14;9 3;10 16; from 10
Agent #9 got 1 13;4 9;6 7;7 14;9 3;10 16; from 10
Agent #6 got 1 13;4 9;6 7;7 14;9 3;10 16; from 9
Agent #9 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 10
Agent #6 sent 1 13;4 9;6 7;7 14;9 3;10 16;
Agent #9 got 4 9;6 7;7 14;9 3;10 16; from 6
Agent #9 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16;
Agent #9 got 1 13;4 9;6 7;7 14;9 3;10 16; from 6
Agent #10 got 1 13;4 9;6 7;7 14;9 3;10 16; from 9
Agent #6 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 9
Agent #10 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 9
Agent #6 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16;
Agent #9 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 6
Agent #7 got 1 13;4 9;7 14; from 4
Agent #7 got 1 13;2 17;3 11;5 3;7 14;8 5; from 2
Agent #7 got 1 13;2 17;3 11;5 3;7 14;8 5; from 2
Agent #7 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;
Agent #7 got 1 13;2 17;3 11;4 9;5 3;7 14; from 4
Agent #7 got 1 13;2 17;3 11;4 9;5 3;7 14;10 16; from 1
Agent #7 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 2
Agent #7 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #4 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 7
Agent #1 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 7
Agent #4 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;
Agent #7 got 1 13;2 17;3 11;4 9;5 3;7 14;10 16; from 1
Agent #7 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;9 3;10 16; from 1
Agent #2 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 7
Agent #4 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16; from 7
Agent #4 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #2 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16; from 7
Agent #10 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 4
Agent #2 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #7 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #4 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 7
Agent #4 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #3 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16; from 2
Agent #2 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 7
Agent #3 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #2 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #10 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #8 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16; from 3
Agent #3 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 2
Agent #3 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #8 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #8 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 3
Agent #8 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #9 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 10
Agent #9 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #6 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 9
Agent #6 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
Agent #5 got 1 13;2 17;3 11;5 3;7 14;8 5; from 2
Agent #5 sent 1 13;2 17;3 11;5 3;7 14;8 5;
Agent #5 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5; from 2
Agent #5 got 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16; from 2
Agent #5 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #5 sent 1 13;2 17;3 11;4 9;5 3;7 14;8 5;10 16;
Agent #5 got 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16; from 2
Agent #5 sent 1 13;2 17;3 11;4 9;5 3;6 7;7 14;8 5;9 3;10 16;
AVR = 9.8
```
