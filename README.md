# DomEx
Extending Protein domain predictors to detect discontinuous domains
DomEx USAGE:
Mandatory arguments:
./DomEx.pl -seqname sequence_name 
Optional arguments:
      -workdir workdir: the work directory.Defaut:'./workspace'
      -b b_value: the cutoff of the parameter b(0.1<=b<=0.9). Default: 0.1.
Users can change these defaut values from line 23 to 31 of DomEx.pl  

For example:
   ./DomEx.pl -seqname Targetname -b 0.3
  
    Notice: 
    (1)the Tegetname.fasta and Targetname.sd should be put in the directory workdir/Targetname.Check the example in the workspace,please. 
    (2)Targetname.sd: The file of  predicted domain segments predicted by any domain predictor. The format is like :targetname\tsequencelenth\tsegmentnum\tsegments\n. If users want to combine DomEx with ThreaDOm, install ThreaDom, and copy the segment prediction result to target.sd.
    (3)The program is designed on the PBS-based cluster. Users have to modify the programs if running on workstation.


For test:
   There is an example in ./output/S50. User can add a task to crontab for multi-call  dDomEx.pl, or excute "./DomEx.pl -seqname S50"  several times mannully.
   User can also check the check.txt file for the running state. 

For users who want to predict domain boundaries by ThreaDom:
   (1)Download ThreaDom package from http://zhanglab.ccmb.med.umich.edu/ThreaDom/ , or subimit your sequence online.
   (2)copy prediction result to Targetname.sd( for example T50.sd)
   (2)excute ./DomEx.pl -seqname Targetname 

About Domain nonreduntant library:
   This library file is too large to upload to github. Users can extract the single domain library from CATH,SCOP,Pfam, or downlaod from http://isyslab.info/DomEx.   

zhidong xue
zdxue@hust.edu.cn


   
