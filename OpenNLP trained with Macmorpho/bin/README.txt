

##########
#Training#
##########

#This version of OpenNLP is already trained with MacMorpho-full corpus.
#To re-train OpenNLP, use the following command, replacing 'macmorpho-full.txt' for a new corpus file name.

opennlp POSTaggerTrainer -type maxent -model pt-pos-maxent.bin -lang pt -data macmorpho-full.txt -encoding utf-8

--------------------------------------------------------------------------------------------



########
#Tagger#
########

#To use OpenNLP to tag sentences, be sure that you have a file with a sentence by line.
#Use the following command to tag a text file. Replace 'input_example.txt' for your input file name. Replace 'output.txt' for a name that you like.

opennlp POSTagger pt-pos-maxent.bin < input_example.txt > output.txt