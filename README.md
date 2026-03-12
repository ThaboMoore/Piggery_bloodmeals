Hi Brendan, Alex and Elle, 

Here are the key scripts from the new MMseqs2 analysis. 

The scripts are in the **Main branch**. 

The full MMseqs2 taxonomy reports are in the **full_taxonomy_reports branch**. 

To make it data extraction easier, I filtered the full taxonomy reports. 
The filter includes all families with over 1% of reads (along with all the genus and species within that family). 

The filtered taxonomy reports are in the branch **filtered_taxonomy_reports**.

MMseqs2_results.xlsx is my interpretation of the results. 
I extracted the genus (or species) with the highest percentage of reads. 
Some samples had multiple genus/species with high read percentages. 

How to read the MMseqs2 taxonomy results
- Column 1 is the percentage of reads from the full sample that align to this taxon
- Column 2 is the number of reads at or below this taxon
- Column 3 is the number of reads associated with that taxon that could be resolved at a lower taxonmy. For example, if Column 2 has a value of "500" and Column 3 has a value of "490" then only 10 reads were not resolved at a lower taxon. In the example below, most of the reads at the family and genus level were able to assigned to a lower taxon. However, you can see that there was not the same confidence at the species level. No species jumps out as having a high percentage of reads. For this example, we would stick to the genus level. 

7.7679	195722	184	    family	9895	        Bovidae
7.0741	178240	177347	genus	9935	          Ovis
0.0095	239	    239	    species	469796	      Ovis orientalis
0.0092	232	    232	    species	3370470	      Ovis gmelinii
0.0074	186	    186	    species	30527	        Ovis ammon
0.0065	164	    164	    species	59896	        Ovis vignei
0.0016	40	    40	    species	703186	      Ovis orientalis x vignei
0.0006	16	    16	    species	9940	        Ovis aries
0.0004	11	    11	    species	56194	        Ovis nivicola
0.0002	5	      5	      species	37174	        Ovis canadensis

In this second example we can be more confident that Sus_scrofa is the correct hit at the species level. 

4.2298	126221	7	family	9821	                                                  Suidae
4.2294	126210	7748	genus	9822	                                                   Sus
3.8775	115710	115710	species	9823	                                                 Sus scrofa
0.0880	2627	2627	species	273789	                                                   Sus celebensis
0.0018	53	53	species	41807	                                                         Sus barbatus
0.0012	37	37	species	159856	                                                       Sus verrucosus
0.0007	20	20	species	315376	                                                       Sus philippensis
0.0003	8	8	species	315378	                                                           Sus philippensis x Sus barbatus
0.0002	7	7	species	315377	                                                           Sus cebifrons
