Extraterrestrial-Irradiance
===========================

This LabView VIs has been developed for teaching and illustration of the Earth-Sun geometry and the distribution of solar radiation in absence of atmospheric effects on flat and tilted (sloped) surfaces (i.e. to calculate extraterrestrial irradiance K<sub>Ex</sub>). This is used in teaching climatology, solar energy, building-atmopshere interactions etc.

Description
--------------

On the top-level VI two graphs are displayed that change with user interaction. User can select latitude, slope angle (tilt) and slope azimuth (exposition of slope) to calculate the direct beam irradiance as a function of time of day and time of year (contour plot) and as a function of time of year for daily totals. 

The flux densities represent the short-wave (solar) irradiance in W m<sup>-2</sup> that would hit a flat or sloped surface at given latitude in absence of atmosphere. The code considers self-shading, but not shading by nearby orography and obstacles. Further it is a simple set of equations that assumes a circular orbit of the planet. Values are approximated using the  set of equations in T.R. Oke 'Boundary Layer Climates' (2nd Ed. Routlegde, Appendix A1, p. 339-342 and 345 to 346, equations A1.1 to A 1.4, and A 1.6 to A 1.8).

A web implementation of this applet in modified for can be found at:
* http://ibis.geog.ubc.ca/courses/geob300/applets/latitude/
* http://ibis.geog.ubc.ca/courses/geob300/applets/slope/

The installation contains the following VI's:

Top-level VI
--------------

* irradiance.vi - calculates the extraterrestrial (direct beam) irradiance as a function of time of day and time of year (contour plot) and as a function of time of year for daily totals for flat and sloped surfaces. 

Sub-VIs
--------------

* declination_angle.vi - calculates the approximate solar declination <i>&delta;</i> in radians at a given time of year using a simplified equation in T.R. Oke Appendix A1.
* hour_angle.vi - calculates the hour angle <i>h</i> in radians for a given mean local time (hours of day since midnight).
* zenith_angle.vi - determines the zenith angle <i>z</i> in radians for a given location (latitude) and time (day of year, time of day).
* azimuth_angle.vi - determines the solar azimuth angle <i>&Omega;</i> in radians for a given location (latitude) and time (day of year, time of day).
* slope_calculation.vi - calculates the cosine of the angle between a slope normal and the solar beam for a given solar zenith angle, slope angle, solar azimuth angle and slope azimuth angle.

Source / License
--------------

This code has been written by Andreas Christen, Associate Professor, the University of British Columbia, Vancouver, Canada and is published for free use and modification under the GNU GPL V 2.0.
