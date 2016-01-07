# Python-Streaming

Examples of Hadoop Python Streaming scenarios

To Run

$ bin/hadoop jar contrib/streaming/hadoop-streaming-1.2.1.jar -file /home/Streaming/word_count_map.py -mapper word_count_map.py -file /home/Streaming/word_count_reduce.py -reducer word_count_reduce.py -input input/ -output output/

To test without Map Reduce:

$ echo "foo bar abd def abc xyz" | /home/Streaming/word_count_map.py | sort -k1,1 | /home/Streaming/word_count_reduce.py
