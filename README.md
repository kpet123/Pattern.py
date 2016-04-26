# Pattern.py
String search functions useful in bioinformatics. Need Biopython package



Pattern.py Module API- lists how to use all functions and classes in Pattern.py

	                                     
1.  isRepeat(test, List)	                             
    
 Looks if "test" is in "List". If yes, return 0, if no, return 1. Also mutates "List" to include test is "test" wasn't in it before
***********

2.  listseqRec(infile)	    

Returns list of seq records from fasta file 
***********

3.  listDef(infile)	

Returns list of seq record descriptions from fasta file


listSeq(infile) 	                                 returns list of sequences from fasta file


discern_ebox(infile)                             	 For known pilli: generates all sequences matching ebox motif from fasta file then prompts user to discern real ones 


writeFromFasta()	                                Outputs hits for given fasta file with particular search parameters


norm(motifcount, seq)	                            normalizes motif count


findEnclosed(string, start, end)	" given a start and end character, returns what is in between. LIMITATIONS: start and end can only appear once in the string
#used to find name of organism from alignment data, name is enclosed by '[' and ']'"

