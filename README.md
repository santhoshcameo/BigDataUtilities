Introduction

As most of them know, working with Big Data is really interesting one, but few of the occasions it's tedious task to find the volume/Size of the directories and its sub directories. 
The volume definer utility is the Hadoop/Big Data Job which will run and produce the     directory wise size (while running the mapper) and produce the total size of the directory while reducer runs.

Volume of Input Data:

Most of the occasion we used process the data in large manner, and we used to analyse the data using our hadoop jobs, but ever we tried how much data we processed? Or how much folders we processed? How much directories the map reduce iterated? The map reduce API gives overall processed data throughout the job.

How this volume definer utility works is given below:

Working 

The Mapper Jobs reads the input path which is given as text file input, and it reads the content of the path from the text file.
The ContentSummary library of hadoop will define the volume in each iteration of the sub directories, it will be written into a text file which is given as an argument as line by line.
The second job reducer will run and it will give the total size of the given input path.

Arguments:

1. Copy the input directory location into a text file and give the text file as first argument
2. Give the output directory where you want to get the text file output.


Benefits

1. It lists all the sub directories of the given path and produces the directory wise output.
2. It produces the total size of the directory when reducer runs.
3. Accept multiple input location by comma separated values and read those contents from the given path and produce the volume respectively.
4. Useful for large sets data's with multiple sub directories.
