# SIP_LEX
SIP_LEX – Message Level SIP Anomaly Detection System

The Session Initiation Protocol (SIP) is at the root of many sessions-based applications such as VoIP and media streaming that are used by a growing number of users and organizations. The increase of the availability and use of such applications calls for careful attention to the possibility of transferring malformed, incorrect, or malicious SIP messages as they can cause problems ranging from relatively innocuous disturbances to full blown attacks and frauds. 

To this end, SIP messages are analyzed to be classified as "good" or "bad" depending on whether this structure and content are deemed acceptable or not. 
LEX_SIP, a novel multi-stage filtering architecture is developed here where message filtering is performed by a lexical analyzer and SVM (Support Vector Machine) classifiers. The first stage is a lexical analyzer to weed out SIP messages with syntax errors. The second stage is based on machine learning techniques, specifically on SVM, to detect SIP messages with semantic errors and harmful content by learning from previous experiences.

Download & Install SIP_LEX
Please download the latest version of 'SIP_LEX' from Github (https://github.com/rferdous/SIP_LEX). After downloading please unzip the compressed file. The compressed file contains : 
1. Jar file of the 'SIP_LEX' application named 'SIP_LEX.jar'. 
2. A configuration file named “input.properties” containing the list of parameters that should be configured before running SIP_LEX. 
3. A sample input file named 'SIP_MSG.txt' containing a set of SIP messages. The set consists of 5000 SIP messages with a balanced mix of 'good' and 'bad' messages. This sample file is located under the folder named “Incoming SIP Messages”. 

Configure SIP_LEX

The first step of using SIP_LEX application is to configure the input parameters which are defined in the configuration file named “input.properties”. The following parameters are mandatory to configure:

    INPUT_FILE_PATH - Path of the input files containing SIP messages
    OUTPUT_SYNTAX_ERROR_LIST - Path of the output file containing the list of SIP messages with syntax error
    OUTPUT_SYNTAX_ERROR_LIST - Path of the output file containing the list of syntactically well-formed SIP messages

Input of SIP_LEX

Input of the SIP_LEX is a set of SIP messages that can be stored in one single file or multiple files. Users should store the input files in a folder and specify the folder name as the parameter “INPUT_FILE_PATH”. End of each SIP messages is indicated by the text “$ENDMSG$” and a newline.
Output of SIP_LEX

SIP_LEX produces two output files:

    List of messages with syntax error
    List of syntactically well-formed SIP messages

Run SIP_LEX

    Set PATH variable - export PATH=$PATH:"Location of the .jar file"
    Browsing the location of SIP_LEX application folder
    Run the jar file of the application : java -jar LEX_SIP.jar

