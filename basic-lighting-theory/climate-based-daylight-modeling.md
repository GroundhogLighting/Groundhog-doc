# Climate Based Daylight Modeling

_The core of this section is based on material contributed by John Mardaljevic \(Loughborough University, UK\)_

Climate-based daylight modelling \(CBDM\) is the prediction of any luminous quantity \(illuminance and/or luminance\) using realistic sun and sky conditions derived from standardised climate data. CBDM evaluations are usually carried out for a full year at a time-step of an hour or less in order to capture the daily and seasonal dynamics of natural daylight. Developed in the late 1990s, CBDM steadily gained traction – first in the research community, closely followed by some of the more forward-thinking practitioners. The widespread adoption of the Radiance lighting simulation system and, ultimately, CBDM was due in part to the outcomes from validation studies.

What is probably still considered the definitive validation study for any daylight prediction method \(physical model, analytical or simulation\) was carried out in the mid 1990s using data collected by the BRE as part of the International Daylight Measurement Programme – the data are sometimes referred to as the BRE-IDMP validation dataset. That study showed that illuminances predicted using the Radiance system could be within ±10% of measured values, i.e. within the accuracy limits of the measuring instruments themselves. This, quite remarkable, degree of precision needs to be judged alongside the high level of inaccuracies \(often in excess of 100%\) that were determined to be fairly typical for physical modelling. The BRE-IDMP dataset was used to validate the daylight coefficient approach in Radiance which is the basis of many CBDM formulations. The author’s \(J. Mardaljevic's\) daylight coefficient implementation was shown to have comparable high accuracy to the standard Radiance calculation. CBDM has been applied to numerous real-world projects in a variety of ways to address ‘traditional’ and novel daylighting issues/problems.

## Relevant publications

* J. Mardaljevic. Climate-Based Daylight Modelling And Its Discontents. CIBSE Technical Symposium, London, UK, 16-17 April, 2015
* J. Mardaljevic. Simulation of annual daylighting profiles for internal illuminance. Lighting Research and Technology, 32\(3\):111–118, 1 2000.
* C. F. Reinhart and S. Herkel. The simulation of annual daylight illuminance distri- butions – a state-of-the-art comparison of six RADIANCE-based methods. Energy and Buildings, 32\(2\):167–187, 2000.
* J. Mardaljevic. Validation of a lighting simulation program under real sky condi- tions. Lighting Research and Technology, 27\(4\):181–188, 12 1995.
* J. Mardaljevic. The BRE-IDMP dataset: a new benchmark for the validation of illuminance prediction techniques. Lighting Research and Technology, 33\(2\):117– 134, 2001.
* S. W. A. Cannon-Brookes. Simple scale models for daylighting design: Analysis of sources of error in illuminance predictiont. Lighting Research and Technology, 29\(3\):135–142, 9 1997.
* J. Mardaljevic. Daylight Simulation: Validation, Sky Models and Daylight Coeffi- cients. PhD thesis, De Montfort University, Leicester, UK, 2000.

