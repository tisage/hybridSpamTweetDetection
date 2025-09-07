The text file contains three columns: tweet_id, label, and step (see sample data on the right). The label field contains one of three values {0, 1, -1} where: 0 is for ham (or non-spam tweet), 1 is for spam tweet, and -1 is for those tweets that can not be labeled as spam or ham even after manual inspection. The step field contains values from 1 to 6, describing at which step the tweet was labeled during the labeling process:
1 => Manual annotationHSpam14 Sample
2 => kNN-based annotation
3 => User-based annotation
4 => Domain-based annotation
5 => Reliable ham tweet detection
6 => EM-based annotation