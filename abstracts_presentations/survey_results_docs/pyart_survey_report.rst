PY-ART ROADMAP SURVEY RESULTS:
==============================

35 people responded to the Py-ART survey, 24 of them used Py-ART 11 of them do 
not.

PEOPE WHO USE PY-ART:
---------------------
                        
**DEMOGRAPHICS OF THE SURVEY RESPONDERS:**

The 24 users that use Py-ART were broken down into three self-selected 
categories, none consider themselves exclusively modelers, seven consider 
themselves hybrid modelers and observers and 17 consider themselves exclusively 
observers.  The three hybrid users that continued to answer questions were 
comprised of two professors and one scientist.  The 15 observers that continued 
to answer the questions consisted of six graduate students, three research 
assistants, four scientist/professionals, one professor and one that did not fit 
any of the categories.  When asked about employment, twelve of the Py-ART users 
that responded that they work at a university, two in the private sector, two 
are non-us government contractors, one directly works for a non-US government 
and one is a US government employee. 

**TECHNICAL DEPLOYMENT OF PY-ART:**

The operating system breakdown for the Py-ART  user community is: 44% Linux, 39%
OSX, 16.7% Windows.  The responders identify that 88.2% of Py-ART installs are 
from the source using Anaconda with ëbinary install from jjhelumus channelí and
ëpip installí garnering 6% each.  17 participants answered this question.

**METHODOLOGY OF THE RANKING:**

A selector dropdown ranks each feature between one and number of options.  
A count of the responses are multiplied against their ranked rank and summed. 
An example score would be three responses for rank 1 would be three points 4 
responses for rank 3 means 16 points added together 19 points.  That sum is 
divided by the total number of responses to that feature giving the feature a 
weighted ranked score, having the lowest score means that feature is the most 
important to the users. The example would yield a rank score of 2.7

**THE WEIGHTED RANKED ORDER OF FAVORITE FEATURE IS:**

1.  Plotting/visualization
2.  Diverse file format support
3.  Dealiasing
4.  Gridding include gridding of multiple radars
5.  As a dependency for CSU_Tools or ARTView or other
6.  Attenuation Correction
7.  Polarimetric phase processing processing (LP) (Tied with 8)
8.  Polarimetric phase processing processing (other) (Tied with 7)
9.  Knowing VAPS developed easily integrate with ADI/ARM systems

**REQUESTED FEATURES IN ORDER BY POPULARITY OF WEIGHTED RANK:**

1.  Multi-Doppler Winds
2.  Cell/Object Tracking
3.  More Bulk statistics of grid or radar contents (CFAD, echo top heights etc..)
4.  More output formats
5.  More input formats
6.  Velocity Azimuth Display wind retrievals
7.  Quasi-Vertical Profile reconstruction from a list of radars
8.  More data quality code (eg clutter rejection, biological masks..)
9.  Ingest of WRF data into the Py-ART Grid Model
10. Add the option of Cartopy map backend to the existing basemap in RadarMapDisplay
11. Easier "One step" rainfall retrievals
12. Ability to handle Radar Spectra and perform retrievals on that
13. More high level retrievals from the literature (Eg DSD, Particle ID..)

**ASKING FOR THE NEXT KILLER FEATURE BY TEXT BOX.**

These comments have no order to them so they are just listed below for reference:
Feature 1 (11 responses): 

- Easier installation
- Dual-Doppler Wind Calculations
- More advanced feature with Cross-section cut, based on any two single points, similar to iris
- Dual-Doppler Winds
- Treat variable like this variable 
- cross sections between any two points
- RadarCollection
- Advection correction
- More precise data model - e.g in Nexrad Level 3 the width of azimuth gates are not always uniform and in the data format the rays are described with "azimuth of the beginning of the ray" and width of the ray. See relevant ICDs on Level 3. 
- Multi-Doppler wind retrievals
- Additional weighting function options when gridding radar data, besides the Barnes and Cressman schemes

Feature 2: (6 responses)

- Dealiasing X-Band Vertical Profiling Radar
- More advanced algorithm, like ZDR column detection or NCAR PID algorithms
- Easier Geotiff compatibility 
- Carry along a map image/background to help speed up multiple plotting instances of same radar
- Improved dealiasing algorithms
- Hydro ID

Feature 3: (3 responses)
Collaboration with SingleDop
Improved dealiasing
Improvements to ARTview to make it replace solo3

**CONTRIBUTIONS BACK TO THE PY-ART COMMUNITY AND CODE:**

There were 18 responses to the question ìHave you ever contributed to Py-ART?î  
Of the 18, 22.2%(4)  said Yes via pull request through Github, 5.6%(1) said yes,
by intellectual property implemented by someone else, 44.4%(8) said no, but 
they wanted to and 27%(5) said no and they werenít interested in doing so. 

When asked what barriers are there to being a contributor the barriers are 
ordered.

1.  Not enough time
2.  I do not think I have done anything worth contributing
3.  I do not understand Git or GitHub
4.  I feel I need to clean the code and add unit tests
5.  Institutional Policies (IP problems)

Items 2,3,4 scored relatively closely ranging between 2 and 3, in contrast to 
"Not enough time" being a strongly ranked 4.13 and "Institutional Policy" was 
given a 1.0 the lowest possible rank.
                    
PEOPLE WHO DO NOT USE PY-ART:
-----------------------------

Eleven participants answered they do not use Py-ART, of those two said they were in 
modeling, two said they were hybrid between modeling and observations and seven
said they were exclusively observers.  The modelers did not answer any further
questions, and only one of the hybrids continued.  That individual is a postdoc 
at a university, who has herd of Py-ART but does not know any team members that 
use it, and does not handle the processing of the data.  This individual may be 
more likely to use Py-ART if Cell/Object Tracking, more data quality code, or 
Velocity Azimuth Display wind retrievals were added.  The largest deterrent from 
using Py-ART is that this post doc does not deal directly with the data.
The three remaining observers consisted of a research assistant and two 
scientist/professionals.  One participant is from a university; one is a 
government contractor (US), and one is an employee of a government but not the 
US government.  All three have heard of Py-ART.


**THE RESPONSE TO THE QUESTION "RANK THESE IN ORDER OF HOW LIKELY THEY ARE TO GET 
YOU INTERESTED IN USING PY-ART":**

1.  More high level retrievals from the literature (Eg DSD, Particle ID..)
2.  Multi-Doppler Winds
3.  Velocity Azimuth Display wind retrievals
4.  Easier "One step" rainfall retrievals
5.  Cell/Object Tracking
6.  Ability to handle Radar Spectra and perform retrievals on that
7.  More Bulk statistics of grid or radar contents (CFAD, echo top heights etc..)
8.  More output formats
9.  Quasi-Vertical Profile reconstruction from a list of radars
10. More input formats
11. Ingest of WRF data into the Py-ART Grid Model
12. More data quality code (eg clutter rejection, biological masks..)
13. Add the option of Cartopy map backend to the existing basemap in RadarMapDisplay

**BARRIERS TO USING PY-ART:**

Nothing scored higher than a 2.5 (neutral is 3).  One user said it is difficult 
to install and that is what stops them, the other said they were using their own
software and were happy with it.

**FREE FORM COMMENTS:**

- Thank you for saving me tireless hours in SOLOIII dealiasing X-band radar data Many thanks to all the developers and contributors of Py-ART I have some radar to WRFDA input code ready to send, but would like some advice on how to do it. Please email me if you have the time, felixswps@gmail.com .
- Would also like to contribute hydrometeor ID and cell identification, tracking, and forecasting code in the future! -Mariana
- Great work!
- Hi, Scott!
- Dealiasing and multi-Doppler wind reteivals would be a huge step forward. Issues with auto dealiasing and lack of multi-Doppler retreivals are the biggest set backs from completely switching to Pyart.
- Py-ART has been immensely helpful to me in my research! Thank you!
