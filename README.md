# HAAD
Human Annotated Arabic Dataset of Book Reviews for Aspect Based Sentiment Analysis
# Dataset
The dataset consists of three files:
1. The training file.
2. The test file.
3. The Test-gold file which will be used as a reference to evaluate your approach result on the Test file using the common evaluation Eval.jar.
# Evaluation
This folder contains scripts/code for:

A. Evaluating the output of your system.
B. Validating the XML file.

To evaluate your results against the Baseline results follow the following:

ava -cp ./eval.jar Main.Aspects test.xml ref.xml

It calculates and displays the precision, recall and F1 for aspect term and category extraction for a system that generated test.xml, comparing it to ref.xml that contains
the gold correct annotations. The same measures are also calculated and displayed by Baseline results.

java -cp ./eval.jar Main.Polarity test.xml  ref.xml

It calculates only the overall accuracy for the polarity detection task, the above command also calculates F1, Precision and Recall 
for all labels (positive|negative|neutral|conflict). As previously, test.xml is the file that the system generated and ref.xml
is the one that contains the gold (correct) annotations.

Before publishing your results, we highly recommend you validate (as shown below) the XML your system produced against the provided XSD schema (SemEvalSchema.xsd). 
This way you will verify that your XML output is well-formed and can be processed/parsed by our evaluation scripts.

java -cp ./eval.jar Main.Valid test.xml  SemEvalSchema.xsd

# Reference
Please cite the following paper if you use HAAD:

Mohammad AL-Smadi, Omar Qawasmeh, Bashar Talafha, & Muhannad Quwaider. Human Annotated Arabic Dataset of Book Reviews for Aspect Based Sentiment Analysis. Proceedings of 3rd International Conference on Future Internet of Things and Cloud (FiCloud 2015), August, 2015, Rome, Italy   

# Contact us

Dr. Mohammad AL-Smadi,   PhD
     Assistant Professor
     Computer Science Department
     Faculty of Computer & Information Technology
     Jordan University of Science and Technology
     P.O.Box: 3030 Irbid 22110, JORDAN
     Tel.: +962-2-7201000   Ext. 23321   Fax: +962-2-7095046   Faculty Fax: 22783
	 E-mail: maalsmadi9@just.edu.jo