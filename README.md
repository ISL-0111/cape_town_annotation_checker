**[Annotation Cheker Pipeline Summary]**

This code handles three tasks:
Cleaning annotation files(db_pipeline/data_processing.ipynb)
Sampling annotations(sample_select_for_qc/annotation_sampling.ipynb)
Annotation quality checking(annotation_checker/checker.ipynb)

**Current Issue **
(June 10, 2025) Final annotation files contain duplicate values and uncertain flags. it's impossible to estimate the accuracy denominator.
Remarks : Our target accuracy threshold is 90%, but the current annotation quality holds up progress.
Therefore, we need to decide whether to (1) remove all entries with uncertflag and duplicate annotations, or (2) explicitly define how to handle them.
Additionally, it is necessary to clarify the impact of processing image tiles in which PV arrays are only partially annotated.


**[Data Overview]**

**Total annotations: 19,735**
PV_normal: 10,787\
PV_heater: 5,216\
PV_pool: 2,503\
uncertflag: 1,920\
Annotations with only uncertflag (no duplicates): 1,231

**Double Annotations**
PV_heater & PV_pool: 2\
PV_heater & uncertflag: 484\
PV_pool & uncertflag: 205\

Refers to Sampling annotations(sample_select_for_qc/annotation_sampling.ipynb)
