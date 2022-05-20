## R CMD check results


## Test environments
- R-hub windows-x86_64-devel (r-devel)
- R-hub ubuntu-gcc-release (r-release)
- R-hub fedora-clang-devel (r-devel)

## R CMD check results
> On windows-x86_64-devel (r-devel), ubuntu-gcc-release (r-release), fedora-clang-devel (r-devel)
  checking CRAN incoming feasibility ... NOTE
  Maintainer: 'John V Colias <jcolias@decisionanalyst.com>'
  
  New submission
  
  Package was archived on CRAN
  
  Possibly misspelled words in DESCRIPTION:
    MNL (7:221)
    
  [MNL is a common abbreviation for Multinomial Logit]
  
  Found the following (possibly) invalid URLs:
    URL: http://www.decisionanalyst.com (moved to https://www.decisionanalyst.com/)
      From: DESCRIPTION
      Status: 200
      Message: OK

> On windows-x86_64-devel (r-devel), ubuntu-gcc-release (r-release), fedora-clang-devel (r-devel)
  checking for non-standard things in the check directory ... NOTE
  Found the following files/directories:
    'RBetas.csv' 'RLH.csv' 'RLog.txt' 'restart.txt'

[The four files mentioned in the note are saved by the choicemodelr function into the current working directory. These files include model outputs (RBetas.csv’ ‘RLH.csv’), a log file (‘RLog.txt’), and parameters needed for restarting the model algorithm at a later date (‘restart.txt’).]

> On windows-x86_64-devel (r-devel)
  checking for detritus in the temp directory ... NOTE
  Found the following files/directories:
    'lastMiKTeXException'
    
    [I have no comment about his note.]

0 errors v | 0 warnings v | 3 notes x
