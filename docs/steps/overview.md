# **General overview**

<a href=../step1 target="_blank"> STEP 1</a> &rarr; Selection of the Point(s) of Interest (POI) from <a href=../../background/neamthm18 target="_blank">NEAMTHM18</a>), using the extension of the local grid or the coordinates of the site of interest or directly the labels of the
desired POIs, if known.

<a href=../step2 target="_blank"> STEP 2</a> &rarr; Scenario Dumping: all of the earthquake scenarios and corresponding metadata that contribute to the tsunami hazard at the target site are extracted from the <a href="The-regional-hazard-model-NEAMTHM18" target="_blank">NEAMTHM18</a> database.

<a href=../step3 target="_blank"> STEP 3</a> &rarr; Scenario Selection: a number of relevant scenarios significantly contributing to the tsunami hazard at the target site is selected. Presently, the implemented procedure is a <a href="Disaggregation" target="_blank"> disaggregation</a> from the total hazard, based on the mean model of the epistemic uncertainty. In the future, other approaches will be implemented, such as the <a href="Sampling" target="_blank"> importance sampling</a>.

<a href=../step4 target="_blank"> STEP 4</a> &rarr; Scenario Annual Rates: the annual rates of occurrence, including the whole epistemic uncertainty, are retrieved for all of the scenarios obtained from the sampling procedure.

<a href=../step5 target="_blank"> STEP 5</a> &rarr; Tsunami Simulations: high-resolution numerical simulations of the tsunami generation, propagation and inundation on telescopic nested grids are set up and executed for each scenario, using the <a href=../../background/Tsunami-HySEA target="_blank">Tsunami-HySEA</a> numerical code.

<a href=../step6 target="_blank"> STEP 6</a> &rarr; Hazard aggregation: the output from each simulation is combined with the scenario rates to calculate the hazard curves on a predefined set of MIH (Maximum Inundation Height) thresholds.

<a href=../step7 target="_blank"> STEP 7</a> &rarr; Visualization: hazard maps for selected average return periods (ARPs) are produced for visualization.
