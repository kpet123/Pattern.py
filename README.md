# Pattern.py
String search functions useful in bioinformatics. Need Biopython package



Pattern.py Module API- lists how to use all functions and classes in Pattern.py

	                                     
1.  isRepeat(test, List)	                             
    
 Looks if "test" is in "List". If yes, return 0, if no, return 1. Also mutates "List" to include test is "test" wasn't in it before
***********

2.  listseqRec(infile)	    

Returns list of seq records from fasta file 
Note: if want to use infile again, must move reading frame back to beginning
***********

3.  listDef(infile)	

Returns list of seq record descriptions from fasta file
Note: if want to use infile again, must move reading frame back to beginning
************

4. listSeq(infile) 

Returns list of sequences from fasta file
Note: if want to use infile again, must move reading frame back to beginning

*************
5. discern_ebox(infile)

Infile: FASTA file of known CnaBs
Prints out every instance of ebox motif, then user is promted to identify the correct instance (based on surrouding AAs)
Returns a list with start index of the ebox in each sequence in the input FASTA file
Note: not in PatternTest.py test file because list already generated and confirmed

**************

6. writeFromFasta()
WORKS WITH DEPRECATED MOTIF SEARCH AND HAS NOT BEEN UPDATED!
Outputs hits for given fasta file with particular search parameters (need hardcoded motif function)

**************

7. norm(int motifcount, Seq seq)	
Returns integer equal to normalizes motif count (number of motifs found divided by length of sequence)

**************

8.  findEnclosed(string, start, end)

Given a start and end character, returns what is in between. LIMITATIONS: start and end can only appear once in the string
#used to find name of organism from alignment data, name is enclosed by '[' and ']'"

