# Pattern.py
String search functions useful in bioinformatics. Need Biopython package



Pattern.py Module API- lists how to use all functions and classes in Pattern.py

	                                     
1.  isRepeat(test, List)	                             
    
 Looks if "test" is in "List". If yes, return 0, if no, return 1. Also mutates "List" to include test is "test" wasn't in it before

2.  listseqRec(infile)	    

Returns list of seq records from fasta file 
Note: if want to use infile again, must move reading frame back to beginning


3.  listDef(infile)	

Returns list of seq record descriptions from fasta file
Note: if want to use infile again, must move reading frame back to beginning


4. listSeq(infile) 

Returns list of sequences from fasta file
Note: if want to use infile again, must move reading frame back to beginning


5. discern_ebox(infile)

Infile: FASTA file of known CnaBs
Prints out every instance of ebox motif, then user is promted to identify the correct instance (based on surrouding AAs)
Returns a list with start index of the ebox in each sequence in the input FASTA file
Note: not in PatternTest.py test file because list already generated and confirmed



6. writeFromFasta()
WORKS WITH DEPRECATED MOTIF SEARCH AND HAS NOT BEEN UPDATED!
Outputs hits for given fasta file with particular search parameters (need hardcoded motif function)


7. norm(int motifcount, Seq seq)	
Returns integer equal to normalizes motif count (number of motifs found divided by length of sequence)



8.  findEnclosed(string, start, end)

Given a start and end character, returns what is in between. LIMITATIONS: start and end can only appear once in the string
Used to find name of organism from alignment data, name is enclosed by '[' and ']'"


9.  reverse(string)

Given a string, will return a string in reverse order (slow, will optimize)


10. CnaBSearch(seq)


Hard-coded search function for the CnaB sequence motif; input sequence, returns list of locations with CnaB motif.  This is used in makePattern_oo.py. Note: although this function is less flexible than the search() function in Motif (described later), it is much faster and thus better to use when large-scale search funtionality is needed. 

11. findStop(seq)

Input DNA sequence, returns sequence terminated after a stop codon. Note: sequence must be in-frame and forward

12. Class Motif
Holds a flexible motif object that can be searched for in sequences. Instantiate with motif string with specific formatting guidelines:
	a. Each position is separated by space
	b. "Any amino acid" denoted by 'x'
	c. if a position can contain mutliple amino acids, input with no space
For example, "a x x t yv" would be a motif with A in the first position, any amino acid in the second and third position, T in the fourth position, and Y or V in the fifth position. Note: not case sensitive. 

Methods in motif: 
	1. printf()
	    prints out motif
        2. search(seq)
            functions the same way as CnaB search (see above) but flexible motif and slower






