# Coursera_Project
###Code Book
National Longitudinal Study of Adolescent Health (AddHealth)
Code Book Sections:
Academics and Education, Self Efficacy, Feelings Scale, Relations with Parents,
Parents’ Attitudes, Personality and Family
###Research Topic
	Is there a correlation between parental relationship and a child’s performance in school?
Hypothesis:  Children of parents with authoritative parents perform better in school.
###Associated Topic
	What effect does the relationship with parents have on a child’s feelings about self?
Hypothesis:  The closer the relationship with parents the better a child’s emotional state.
###Code
/*  define my library  */

libname mydata "/courses/d1406ae5ba27fe300" access=readonly;

/*  label several key variables  */

data addhealth;

set mydata.addhealth_pds;

label        h1wp9='Close_to_Mother'   h1wp10='Mother_Cares'   h1wp13='Close_to_Father'   h1wp14='Father_Cares';

/*  sort by key  */

proc sort data=addhealth;
                 by aid;

/*  generate frequencies for the key variables selected  */

proc freq ;

tables      h1wp9   h1wp10   h1wp13   h1wp14;

run;
 
###Results
 

###Summary

####How Close Do You Feel to Your Mother

The values this variable can take scale from 1 (not at all) to 5 (very much). A large majority, approximately 84%, indicate that they are quite a bit or very close to their mother (values 4 and 5). Only two people refused to answer (value 6) and three people didn’t know (value 8), but almost 6% indicated no mother (value 7).

####How Much Do You Think She Cares About You

The values this variable can take scale from 1 (not at all) to 5 (very much). A large majority, over 91%, indicate that their mother cares quite a bit or very much (values 4 and 5). Only one person refused to answer (value 6) and three people didn’t know (value 8), but almost 6% indicated no mother (value 7).

#### How Close Do You Feel to Your Father

The values this variable can take scale from 1 (not at all) to 5 (very much). A majority, approximately 56%, indicate that they are quite a bit or very close to their father (values 4 and 5). Only four people refused to answer (value 6) and one person didn’t know (value 8) but 30% indicated no father (value 7).

####How Much Do You Think He Cares About You

The values this variable can take scale from 1 (not at all) to 5 (very much). A majority, approximately 66%, indicate that their father cares quite a bit or very much (values 4 and 5). There were three people who refused to answer (value 6), one person didn’t know (value 8) and one person said not applicable (value 9), but as before 30% indicated no father.

