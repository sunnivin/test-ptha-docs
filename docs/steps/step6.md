# **STEP 6: Hazard aggregation**

This step generates a new folder called `HAZARD` in the working directory and calculates the hazard curves at
each point of the local finest grid for different percentiles of the epistemic uncertainty, by combining the output of each simulation from <a href=../step5 target="_blank">STEP 5</a> with the scenario rates retrieved in <a href=../step4 target="_blank">STEP 4</a>.

To speed up the process, this step is parallelized on the domain, through a horizontal decomposition (along the y direction) of the grid in "slices", which are then processed in parallel, so that each process manages only the points within one slice. The number of slices (i.e. the number of parallel processes) is computed at runtime by the workflow, but the maximum allowed number must be declared in the <a href=../../instructions/json_input target="_blank">JSON input file</a>, as a trade-off between parallelism and manageability. Finally, all the results are recombined.

The code is available both in Python and MATLAB, and the user can choose the preferred language in the <a href=../../instructions/json_input target="_blank">JSON input file</a>, also depending on the software available on the cluster in use.
