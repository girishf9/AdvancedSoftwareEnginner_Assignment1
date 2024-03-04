# AdvancedSoftwareEnginner_Assignment1

Implement a Pseudo Distributed Word Count Application in Python 
NOTE: This assignment should be done and submitted independently. Plagiarism will not be tolerated. Ensure that your work is original, and any external sources are properly cited. 
Assignment Overview: 
In this assignment, you will implement a pseudo-distributed word count application using Python. You will use Python's `multiprocessing` and ` threading` module to parallelize the processing of a large text dataset and aggregate word counts across multiple nodes. This assignment will provide hands-on experience with distributed computing concepts and parallel programming. 
Before staring, read the below article to understand MapReduce’s word count application. 
https://www.analyticsvidhya.com/blog/2022/05/an-introduction-to-mapreduce-with-a-word- count-example/ 
1. Assignment Tasks:
Task 1: Dataset Splitting
1.1Create a large text file that has multiple paragraphs. Include the large text file in 
the submission. 
2.	1.2.  Go to the https://www.browserling.com/tools/word-frequency to find out the frequency of each word. Take a screenshot for the output and paste it in your report. 
3.	1.3.   Implement a Python script to split the text file into multiple (at least two) small text files. Each small text file should have exactly one paragraph. Name each small text file with a unique name. 
Task 2: Distributed Word Count 
2.1.  Implement a word count program using Python's `threading` module. Each thread should perform the following steps: 
- Read a small text file.
- Tokenize the text into words.
- Count the occurrences of each word.
- Return a dictionary of word counts for that small text file. 

2.2. Modify the program to be able to run on multiple processes, where each process can be created using the Python “multiprocessing” module. Each process should run more than one thread in parallel. Each process also needs to aggregate the dictionary returned by all its threads. 
Task 3: Aggregation and Reporting 
3.1. Implement a master process that coordinates the word count aggregation. The master process should: 
- Launch the worker process (described above) to process small data. 
- Collect word count results from all worker nodes. (Note: You need to wait until all the processes are complete before collecting results from worker nodes) 
- Aggregate the word counts into a global word count dictionary. (Note: Processes are isolated from each other. So, you need to find a way to support the inter-process communication.) 
3.2.Generate a final word count report containing the total count of each word across all small text files. Take a screenshot of the final output and paste it into the report. 

