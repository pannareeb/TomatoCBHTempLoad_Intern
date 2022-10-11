# Intern_tomato_KMUTT
There are two main code files (added in this folder as R notebook (.Rmd) file)
# Sugarcollectionmod.rmd - contains 3 sugarmod models
  sugarmod: the model first developed from the paper Chen et al., 2020
    Use data from 2003
    Only for checking that the code works, not actually use for my internship project
  sugarmodH
    Case 1: for all 4 treatments (CC,LL CC,HL HH,LL HH,HL)
    Case 2: for 2 control treatments (CC,LL CC,HL)
  sugarmodH_Ad
    Case 2: for 2 heated treatments (HH,LL HH,HL)
  *sugarmodH_Ad_W and sugarmodW were not used 
# Output-HLvsLL 02.rmd -  a pipeline (calling sugarmods)
  Part 0: Introduction
  Part 1: Import raw data
  Part 2: Forming inputfun
    Part 2.1: Forming `inputfunH`, `inputfunL`
    Part 2.2: Forming `inputfunH_H`, `inputfunL_H`
  Part 3: Running model
    Part 3.1: Create two temperature pattern (HH and CC)
    Part 3.2: [Case 1] Varying temperature and run the model, assuming no change in FW and DW
    Part 3.3: [Case 2] Varying temperature and run the model, assuming a change in FW and DW
    Part 3.4: save them as "OutputModelArrayHLLLnonadjust.csv" and "OutputModelArrayHLLLad1.csv
  Part 4: Compare the two cases
    10 graphs produced in total
    Each should be described
