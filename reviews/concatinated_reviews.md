Reviewer 1:

As  you know, I am an enthusiastic user of Py-ART, which has allowed me to leverage the information provided by polarimetric weather radars without having a formal education in radar meteorology. This is Py-ART’s greatest strength but also potential source of trouble… more on that later. To answer your points:
1. Work to compare and improve phase processing algorithms is incredibly valuable, and would directly impact my own work. KDP is one of the most valuable quantities from polarimetric radars, but is also very sensitive to how it is estimated from total differential phase shift. This alone would improve my ability to do science with differential phase, and have confidence in the conclusions I draw from analysis of KDP. 

Improvements to the mapping backed are very valuable — I often use basemap, but am never 100% satisfied with it. 

Support for radar spectra, and perhaps expanded capability to do spectral dealiasing would be excellent! I think this would open Py-ART up to a whole different community of researchers who would hopefully contribute their algorithms, etc. 

1/2:
The capability to track is certainly extremely helpful, and I already use Py-ART-processed fields together with an open-source tracking toolbox (TrackPY). I have found this to be relatively straightforward, and so I think the real added value in adding this capability to Py-ART is in rigorous testing of tracking methodologies, and some general recommendations and guidelines for tracking objects in radar fields. This is crucial, because in my own limited experience the performance of a tracking algorithm is strongly dependent on the system in question and the scanning strategy of the radar. 

2.
Multi-Doppler wind retrievals can be helpful, but I worry about modelers using Py-ART’s ability to produce such retrievals as a “black box” without being fully aware of the uncertainties associated with the retrievals, and how they depend on the configuration of the radars that are used in them. Again, I think a crucial component of this added capability is clear examples and recommendations for the use of these methods. 
Volume summary statistics such as CFADs are a strange goal for Py-ART. If a researcher is not able to do this for themselves, what confidence is there that they can determine (or are aware of) radar calibration errors or radar uncertainties due to noise, resolution, scanning, etc.? I know modelers like these things to compare their simulations to, but I worry that making it too easy might lead modelers to avoid (crucial! necessary!) collaboration with radar meteorologists. 

3. I think routines for QC would be good. Some of that is mentioned with advection correction, dealiasing, etc. But perhaps some way of doing comparison when multiple radars view a volume? Or looking at Z/ZDR to get some handle on ZDR calibrations? Maybe this is getting too wonky for the purposes of Py-ART. At the very least such functionality would provide tools for the non-expert to explore questions of radar data quality. 

Hope this is helpful! I really do value Py-ART highly and hope to contribute in the coming years!


Reviewer 2:
In general, the roadmap looks good to me. There are many things that are mentioned that I would also highlight, particularly the need for MultiDop, the ability to ingest gridded objects from other sources (such as Radx2Grid or WRF data output), and cell tracking. I will address these below, as well as provide some background on what we currently use the most. In my opinion, PyART needs to be a stable, well-documented, easy-to-use interface with radar data which will elicit more climatological-level studies (rather than cases), and things like the higher order retrievals (rainfall and DSD stuff) can be where the community tools are added on.

Background / where I’m coming from:
As a group here at CSU, we mostly use Py-ART to do quicklooks and initial data processing. I would say that most often we are using the automatic unfolding features, coupled with ArtView to unfold any errors or difficult cases. For our purposes, the higher level functionality is stuff that we have in-house code for (e.g. CSU-Radartools), and many of us work with gridded data and do not use the gridding functionality of PyART (not that it’s not useful, we have other dependencies we are working with). Personally, I have used PyART to select radar gates over a disdrometer, and most often I am coupling PyART with CSU-Radartools for analysis. We do a lot of dual-Doppler analysis, so one limitation on our use of PyART was dependencies down the line in formats for our old code (CEDRIC), but of course an integrated package like MultiDop would greatly streamline that. If we could have a streamlined read data in, perform QC, unfold velocity, grid, and do dual-Doppler, we would save significant time with each analysis, especially with new students.  I would think we could probably save 10 person hours per analysis if we didn’t have to fight formatting issues and old error codes that we currently do.

Thoughts on the 5 year road map:
With the availability of the NEXRAD data from the cloud and the ease of reading it with PyART, I think there is going to be a lot of science that can be done on longer time scales. Additionally, as ARM gets longer-term radar datasets, it’s going to be more important to move away from case studies to larger “climatologies”, which is going to need a framework for reading and processing large datasets. Synergy between models and observations is going to be increasingly more important in the coming years. To this end, I think Py-ART is well suited to be the framework that can handle these things. Therefore, I think the important things to focus on are many of the same issues that emerged from the survey:
1) Cell/ Object tracking. This will be important for studies on the climatological scale.
2) Multi-Doppler wind retrievals. For my own use, this is an incredible road block and something that always takes a significant amount of time in both setting up, running, and explaining to others the methodology and steps. To have an integrated processing from QC -> gridding -> dual-Doppler would save SIGNIFICANT time and effort. While this is mostly a research-level product, it will become much more important for ARM as the SGP radars begin collecting data (such as the multiple-X-bands).
3) Ingesting model data and other gridded data to the Py-ART grid model. This will elicit studies that directly allow radar and models to be cross-compared.
4) Visualization. A strong point of PyART is the visualization ability, so this should continue to be an important part of the development. I agree that random cross-sections between two points would be a fantastic tool.
5) Toward the goal of longer term climatologies, things like dealiasing, and attenuation correction will be important tools as they need to be folded in to the processing.

It is my opinion that the higher order functionality such as rain rate calculations, DSDs, HID, QVPs, VADs, etc. should be lower priority for two reasons. 1) These are generally retrievals that are developed by various researchers, and therefore can be contributions or add-ons to PyART (via things like CSU-Radartools). There are often different methodologies available, and they are under continual development. 2) These are things that can be easily added on to an analysis. That is, after data has been Qced and gridded, one can easily calculate statistics like CFADs, echo top heights, 40 dBZ echo volumes, etc. through simple code, especially if cells have been tracked and identified. Same with things like HID and rainfall, those can easily be applied to gridded data. 

In my opinion, the value of PyART is streamlining reading and processing large amounts of radar data, which includes being able to read many formats, quickly visualize them, do standard processing such as attenuation correction, dealiasing, and gridding. Multiple Doppler functionality is high value because it is much needed in the community, and for this researcher would be very, very high impact. However, for the larger community, there are very few dual-Doppler networks currently. BUT, as ARM is working toward having the X-band dual-Doppler network at SGP, this would be a high priority for being able to work with that data. 

Reviewer 3
1)  Which of the proposed capabilities are most useful to you in your science? If any of the proposed items were available what impact would they make (for example save me 40 hours per year).

Overall, I think the plan makes sense. If phase processing and attenuation correction algorithms can be improved along with polarimetric quality control, then that is great. These are things have can have significant impact on retrievals, but wouldn’t be done by a non-radar scientist unless there are straightforward functions to do this like there currently are in Py-ART. Also, there clearly needs to be a map background, so if the current one is losing support, it is logical that another one needs to be implemented.

Object tracking would be very useful in that other software is not necessarily straightforward to use, so if Py-ART can have a user-friendly algorithm implemented, possibly with selection and tracking options, this could end up being widely used. Multi-Doppler retrieval support is also useful, although it would be nice if there were a baseline multi-Doppler retrieval implemented, since this is not a straightforward retrieval. It sounds like a package is being developed that will depend on Py-ART, which is great. Most people will not be performing multi-Doppler retrievals unless it is somewhat straightforward to do, so if this is possible with a number of laid out options and steps, it would probably be widely used.

It seems like the primary argument for volume summary statistics (CFADs, echo tops, VADs, QVPs) is to reduce data volume for guiding further data discovery, although I think that further data discovery would probably be best served by simply have pre-generated quicklook plots, which exist for many ARM datasets, but not many of the radar datasets. I can also see the volume statistics being useful for model evaluation, although it is important in model evaluation to compute the statistics from model output in the same manner. The same goes for object tracking.

It seems like radar spectra could become very important for model validation in the near future, and this is something that ARM could help lead the way on, so it makes sense to start working on some functions to deal with it.

2) In your view are any of the items proposed are poorly targeted at the ARM stakeholder community? Or which items do you see as least useful to you or the ARM stakeholder community? Given we are resource constrained we need to hear what is NOT useful so we target high impact items.

I think that all of the proposed tasks would be useful to ARM stakeholders, so it really comes down to how much time is involved in each task versus the perceived impact of each, and it is unclear to me based on the roadmap how much time is being proposed for each task.

3) Is there any additional functionality in Py-ART you would like to see that is not listed in the roadmap? What is the one new thing that Py-ART could do to accelerate your use of ARM data or contribute towards ARM’s mission of improving the representation of Clouds and Aerosols in models?

To fully realize the potential of summary statistics and object tracking, it should be possible to read in a model reflectivity Cartesian grid (e.g., from WRF netCDF) and run the same functions on it. If it is not clear how a statistic is being computed for observed radar data, then model-observation comparisons are better served by writing a separate program outside of Py-ART to compute statistics. Therefore, I encourage adding functionality to ingest model output such as WRF netCDF Cartesian gridded output. 

There is also the consideration of comparing observed and simulated radar variables, but this often requires a radar simulator. If a radar simulator package could be linked to Py-ART in that Py-ART could read in its output, which would be probably very similar to that of typical model output (e.g., WRF netCDF), then comparing models and observations in radar variable space would be more straightforward.

It is also advantageous to validate some radar retrievals of geophysical variables (like those outputted by a model) by running the retrievals on model output (e.g., running a multi-Doppler wind retrieval on WRF output and comparing it to actual WRF winds; or running a retrieval like that in Williams (2016) on model output to test whether collision-coalescence and evaporation processes are being effectively retrieved with vertically pointing radar spectra). Of course, there are many levels of complexity as to how a retrieval can be run on model output, and it is usually not possible to sample the model as in reality (e.g., because of limited output times). That said, this also requires the ability to ingest model output into the Py-ART grid model.

A more straightforward comparison of model output with observations involves radar retrieval of model outputted geophysical variables (DSDs, winds, processes, etc.), which does not require Py-ART ingest of model output. There are several useful retrievals not included in Py-ART, but it seems like these can be linked in with other packages listed in Appendix 2 already. If this is the case, it would be useful to clearly link to these packages on the Py-ART website main page, as this will likely increase the usage of Py-ART, as compared to RadX, which has some of these retrievals (e.g., PID, VAD, etc.) built into it already. My point here is that a non-radar scientists typically doesn’t know all of the software packages available to them, and it requires time to figure this out, so if Py-ART can become the one stop shop, so to speak, people will preferentially use it because it is straightforward and saves time.

4) Any other feedback you may have.






