mkdir wordcount_classes
javac -classpath hadoop-core-0.19.0.jar -d wordcount_classes WordCount.java
jar -cvf /home/musigma/MapRed.jar -C wordcount_classes/ .


$ hadoop fs  /home/ms/MapRed.jar org.myorg.WordCount input output (run application after creating txt files in input folder in hdfs)

$ hadoop dfs -cat output/part-00000  (to check output)


