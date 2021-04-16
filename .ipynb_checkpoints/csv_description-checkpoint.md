#### CSV files
Each csv file corresponds to one of four main scenarios:
+ outbreak_cluster_size_oz: qld baseline transmission - cluster seeding strategy 
+ outbreak_cluster_size_uk: uk transmission - cluster seeding strategy 
+ outbreak_poisson_lambda_oz: qld baseline transmission - poisson seeding strategy 
+ outbreak_poisson_lambda_uk: uk transmission - poisson seeding strategy 

#### Description of each column in the .csv files

`outbreak::Boolean::`
whether an outbreak was detected on the median timeseries of new daily cases/diagnoses. Median timeseries is calculated over 1000 simulations.

`outbreak_day::Integer::`
number of days that went by until an outbreak is detected. Estimated from median timeseries of new daily cases.

`outbreak_day_av::Float::`
average number of days that went by until an outbreak is detected. Average estimated over outbreak_day values of individual runs that had an outbreak.

`outbreak_day_md::Integer::`
median number of days that went by until an outbreak is detected. Median estimated over outbreak_day values of individual runs that had an outbreak.

`outbreak_day_sd::Float::`
standard deviation of number of days that went by until an outbreak is detected. Standard deviation estimated over
outbreak_day values of individual runs that had an outbreak.

`outbreak_prob::Float::`
proportion of simulations (out of a 1000) that had an outbreak. Expressed in %.

`control_prob::Float::`
proportion of simulations (out of a 1000) that did not have an outbreak, but had some cases. Expressed in %.

`contained_prob::Float::`
proportion of simulations (out of a 1000) that did not have any cases over the course of the simulation. Expressed in %.

`iq_factor::Float::`
isolation and quarantine factor. Can be roughly interpreted as quarantine “leakage” and 1-iq_factor as quarantine “compliance”.

`cluster_size::Integer::`
number of incoming infections seeded on day 0 of the simulations. Only applicable to scenarios where incoming infections were seeded with the cluster strategy.

`poisson_lambda::Float::`
average number of daily incoming infections. Represents the parameters λ\lambdaλ of a Poisson process. Only applicable to scenarios where incoming infections were seeded with the Poisson strategy.

`num_tests::Integer::`	
daily number of tests

`label::String::`
human readable label identifying the infection seeding strategy

`beta::Float::`
global transmissibility

`first_case_day::Integer::`	
number of days that went by until the first confirmed cases is detected. Median timeseries is calculated over 1000 simulations.

`first_case_day_av::Float::`
average number of days that went by until the first confirmed case is detected. Average estimated over first_case_day values of individual runs.

`first_case_day_md::Integer::`	
median number of days that went by until the first confirmed case is detected. Median estimated over first_case_day values of individual runs.

`first_case_day_sd::Float::`
standard deviation number of days that went by until the first confirmed case is detected. Standard deviation estimated over first_case_day values of individual runs.

`first_case_inf::Integer::`
number of infections on the day the first case is detected. Median timeseries is calculated over 1000 simulations.

`first_case_inf_av::Float::`	
average number of infections on the day the first case is detected. Average estimated over first_case_inf values of individual runs.

`first_case_inf_md::Integer::`
median number of infections on the day the first case is detected. Median estimated over first_case_inf values of individual runs.

`first_case_inf_sd::Float::`
standard deviation of number of infections on the day the first case is detected. Standard deviation estimated over first_case_inf values of individual runs.

`resurgence::Boolean::`
whether a resurgence occurs on the median timeseries of new infections. Median timeseries is calculated over 1000 simulations.

`resurgence_day::Integer::`	
number of days that went by until an resurgence occurs. Estimated from median timeseries. Median timeseries is calculated over 1000 simulations.

`resurgence_day_av::Float::`
average number of days that went by until an resurgence occurs. Average estimated over resurgence_day values of individual runs where a resurgence occurred.

`resurgence_day_md::Integer::`
median number of days that went by until an resurgence occurs. Median estimated over resurgence_day values of individual runs where a resurgence occurred.

`resurgence_day_sd::Float::`
standard deviation of number of days that went by until an resurgence occurs. Standard deviation estimated over resurgence_day values of individual runs where a resurgence occurred.

`resurgence_prob::Float::`
proportion of simulations (out of a 1000) that exhibit a resurgence. Expressed in %. Day 0 is not taken into account.

`resurgence_control_prob::Float::`
proportion of simulations (out of a 1000) that do not fit the definition of resurgence but had nonzero new infections. Expressed in %. Day 0 is not taken into account.

`resurgence_contained_prob::Float::`
proportion of simulations (out of a 1000) that have no new infections. Expressed in %. Day 0 is not taken into account.
