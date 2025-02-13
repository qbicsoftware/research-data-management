# Confounding Variables

!!!info
    _"Confounding, sometimes referred to as confounding bias, is mostly described as a ‘mixing’ or 
    ‘blurring’ of effects. It occurs when an investigator tries to determine the effect of an 
    exposure on the occurrence of a disease (or other outcome), but then actually measures the effect 
    of another factor, a confounding variable."_
    
    Jager, K. J., Zoccali, C., MacLeod, A., & Dekker, F. W. (2008). Confounding: What it is and how to deal with it. Kidney International, 73(3), 256-260. [https://doi.org/10.1038/sj.ki.5002650](https://doi.org/10.1038/sj.ki.5002650)

### Define confounding variables in your experiment

In order to work with confounding variables, first you must define them.
Confounding variables are experiment-specific. Currently, it is not possible to reuse the same 
variable in other experiments metadata in Data Manager.

Confounding variables are defined in your experiment, so navigate to your experiment first.
There you can find the controls to add new confounding variables.

### Assign levels of a confounding variable to your sample

To get the full potential and account for effects of confounding variables in your experiment, you 
can now annotate the samples with your observation of the variables' manifestation.
In contrast to experimental variables, not all samples need to have a level in one confounding variable.

After [defining the confounding variables in your experiment](#define-confounding-variables-in-your-experiment), 
the confounding variables are added in the sample registration and sample editing process. 
In the sample registration and sample editing processes, you have the possibility to annotate 
samples with levels for the confounding variables.

### Rename a confounding variable

To remove a confounding variable, navigate to your experiment, locate the confounding variables editing and rename your confounding variable.
After renaming a variable, the levels are preserved and only the name of the confounding variable are changed.

### Delete a confounding variable

To remove a confounding variable navigate to your experiment, locate the confounding variables editing and remove the variables you want to delete.

!!!warning
    Removing a confounding variable will delete all annotated levels of that variable on all samples in your experiment.
