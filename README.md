# ChoiceModelR
The ChoiceModelR package includes the function choicemodelr that implements an MCMC algorithm to estimate a hierarchical multinomial logit model with a normal heterogeneity distribution.  The algorithm uses a hybrid Gibbs Sampler with a random walk metropolis step for the MNL coefficients for each unit.  Means of the distribution of heterogeneity can optionally be modeled as a linear function of unit descriptor variables.

The dependent variable can be either discrete or a share.  If the dependent variable y_i is a share (0 to 1 inclusive), instead of discrete (1 ,..., nalt; where nalt is the number of alternatives in choice set), then each choice observation is replicated wgt times with alternative i chosen in wgt*y_i observations.  Independent variables can be continuous or discrete, with order constraints imposed on estimated coefficients.

The basic structure of the code for this algorithm was derived from the rhierMnlRwMixture program of the bayesm package available at cran.r-project.org.  Significant modifications were made to greatly reduce the run time, to allow constraints on estimated parameters, handle varying number of choice observations, handle varying number of choice alternatives within each choice scenario, and to optionally allow the dependent variable to be a share (between 0 and 1) instead of discrete (1 ,..., nalt; where nalt is the number of alternatives in choice set).

Note: Version 1.3.0 adds two new features to version 1.2:
(1) Files RBetas.csv, RLog.txt, and restart.txt are saved to a directory specified by the argument, directory, of the choicemodelr function.
(2) choicemodelr also saves the RLH values for each unit to the choicemodelr output object and to an RLH.csv file (saved to the specified directory).
