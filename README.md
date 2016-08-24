The aim of this project is to detect sarcasm in tweets
The data files used are Mature.train and Joy.train
The class labels used in these files are
0	Non_Sarcasm
1	Sarcasm
2	Sentiments

The project consist of 4 files:
1. preprocess.py - used to preprocess the tweets before classification
2. word2vecTest.py - used to train and save word2vec vectors for the data file
3. project.py - used to implement the MVME algorithm and hence helps in designing the kernel matrix
4. main.py - the main file, used to execute the project.
5. tweetDownload.py - used to download the tweets using the tweet ID and save all the tweets into a file.

So do not need to execute the tweetDownload.py file as the tweets have already been downloaded and saved in the data files mentioned above.
It is part of the folder just for reference. Also the Twitter API details have been removed from the file, hence the file wont execute successfully.

The entire file is read by the main.py file and is split into 80:20 for training and testing
To the run the project following steps should be followed.
1. You need to train the word2vec vectors for the data. For that execute word2vecTest.py
2. Speccify the data file to be used in the driver method at the end of the word2vec.py file.
3. This would train the word2vec vectors and save them to a file with the target word
	example: for atrget word mature the word2vec vectors would be saved to modelWord2Vec_mature.file
4. After the vectors are trained we can start the classification process.
5. For classification execute main.py
6. As before change the data file name in line 45 of main.py to change the target word.
7. Similarly change the word2vec model to be used in line 12 of project.py
8. The main.py file will give an execution trace for the entire classification process and will output the classification accuracy before stopping.

Currently the project is running for the target word - mature.
Execution for the target word joy - takes about 50-60 odd minutes, whereas the execution time taken for mature is about 10-15 minutes.
This is strictly down to the data size.
