# Intern_tomato_KMUTT
This is an internship project, carrying out over 2 months in 2022, with the Research assistant at Center for Agricultural Systems Biology (CASB), King Mongkut's University of Technology Thonburi, Thailand.

## SUGAR model and data
SUGAR model here based on pseudocodes given in a paper Chen, J., Vercambre, G., Kang, S., Bertin, N., Gautier, H., & Génard, M. (2020). Fruit water content as an indication of sugar metabolism improves simulation of carbohydrate accumulation in tomato fruit. Journal of Experimental Botany, 71(16), 5010–5026. https://doi.org/10.1093/jxb/eraa225
## Explanation of two R codes
There are two main code files (added in this folder as R notebook (.Rmd) file)
1. ModelCollection.rmd - contains 3 sugarmod models
   1. sugarmod: the model first developed from the paper Chen et al., 2020
      1. Use data from 2003
      2. Only for checking that the code works, not actually use for my internship project
   2. sugarmodH
      1. Case 1: for all 4 treatments (CC,LL CC,HL HH,LL HH,HL)
      2. Case 2: for 2 control treatments (CC,LL CC,HL)
   3. sugarmodH_Ad
      1. Case 2: for 2 heated treatments (HH,LL HH,HL)
   4. Further details: Look at Method in FinalSlidePannaree.pptx (p.10-11)
   5. *sugarmodH_Ad_W and sugarmodW were not used 
2. ModelUsage.rmd -  a pipeline (calling sugarmods)
* Part 0: Introduction
* Part 1: Import raw data
* Part 2: Forming inputfun
   * Part 2.1: Forming `inputfunH`, `inputfunL`
   * Part 2.2: Forming `inputfunH_H`, `inputfunL_H`
* Part 3: Running model
   * Part 3.1: Create two temperature pattern (HH and CC)
   * Part 3.2: [Case 1] Varying temperature and run the model, assuming no change in FW and DW
   * Part 3.3: [Case 2] Varying temperature and run the model, assuming a change in FW and DW
   * Part 3.4: save them as "OutputModelArrayHLLLnonadjust.csv" and "OutputModelArrayHLLLad1.csv
* Part 4: Compare the two cases
   * 10 graphs produced, each with the description
