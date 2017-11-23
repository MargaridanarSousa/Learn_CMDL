## learn_cmdl

learn_cmdl is a Java implementation of a score-based learning algorithm for Bayesian networks. A new proposed scoring functions called **Complete minimum description length** is implemented. The program receives a data set with multivariate categorical observations and outputs the optimal structure, found by the greedy hill climber(GHC).

## Usage 

The algorithm receives a .csv file such that:
1. the first row of each column corresponds to the name of an attribute;
1. the other rows correspond to observations of that attribute. 

By executing the following .jar file:
```
$ java -jar learn_cmdl.jar
```

The  command-line options are the following:
```
--inputFile <file>        Input CSV file to be used for network
                              learning.
--scoringFunction <arg>   Scoring function to be used: CMDL, MDL,
                              LL and K2. CMDL is used by default.
                              
--numRestarts <int>       Number of random restarts for the greedy 
                               hill climber(GHC).

--outputFile <file>       Writes output to <file>. If not supplied,
                             output is written to file 'ouput.dot'.
```
## Example
```
java -jar learn_cmdl.jar led.csv MDL 10 out_led
```










