From a given input of cards, the Missing Cards can be found using the MissingPokerCards java program. Name and number of the cards are in the input; the missing cards are displayed in the output. 


The missing poker cards from the deck of cards indicated in input1.txt will be located by this Map Reduce Program, which will also provide output in the out folder.

The system needs to have the following:

- Hadoop or cloudera installed in the system

- Java installed in the system

Enter the following commands: 

# This command is to create a new directory in hdfs where the input file will be stored. 
hdfs dfs -mkdir /inputfolder

#Instead of <path>, enter the path where the file is located. 
hdfs dfs -put /home/<path>/input1.txt /inputfolder

# This command displays the data of the input file. 
hdfs dfs -cat /inputfolder/input1.txt 

#Instead of <path>, enter the path where the file is located. 
# This command runs the MissingCards.jar file and uses the input1.txt file as the input and stores the output in the #out folder. 
hadoop jar /home/<path>/MissingCards.jar MissingPokerCard /inputfolder/input1.txt /out 


hdfs dfs -ls /out 


#Running this command will display the output
hdfs dfs -cat /out/part-r-00000  


# User can see the output that is missing poker cards

