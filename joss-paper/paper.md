---
title: "SounderPy: An atmospheric sounding visualization and analysis tool for Python"
tags:
  - Python
  - meteorology
  - atmospheric sciences
  - data analysis
  - weather data
authors:
  - name: Kyle J. Gillett
    orcid: 0009-0001-5528-5037
    affiliation: 1
    ror: 04a5szx83
affiliations:
  - name: John D. Odegard College of Aerospace Sciences, University of North Dakota, United States
    index: 1
date: 3 March 2025
bibliography: paper.bib
---


# Summary

SounderPy is a simple, open-source Python package for retrieving, processing, and
visualizing atmospheric sounding data. Designed for simplicity and reliability, SounderPy aims
to provide a uniform and intuitive method for sounding analysis across various data
sources. 

# Statement of need

Meteorological data from diverse sources are often stored in various file
formats and structured in various ways, posing challenges for consistent and
efficient data processing. This complexity and diversity complicates the thorough
analysis of atmospheric properties needed in describing the past, current, and future
state of the atmosphere. 

Normalizing the analysis of meteorological data ensures that meaningful comparisons 
can be drawn across a variety of datasets. From this, reliable statistics and analogs
can be developed, improving pattern recognition and situational context. For example, 
comparing numerical weather prediction (NWP) output to past observations allows 
forecasters to recognize patterns and draw connections between historical and future
events, or to determine the accuracy & reliability of NWP products.

SounderPy addresses these challenges by providing simple access to multiple data sources,
including National Weather Service radiosonde observations (RAOBs), Aircraft Communications 
Addressing and Reporting System (ACARS) data, NWP forecast data, and several reanalysis 
datasets. Each of these data types come with unique file formats and data-structures. After 
requesting data, SounderPy will process and output the data as a Python dictionary, coined 
a "SounderPy `clean_data` dictionary". Doing so means that every data source ends up in 
a uniform format for analysis and visualization.


# High-level API overview

Simple, intuitive classes and functions make SounderPy's API easy to understand and
use. The procedure for creating sounding figures requires only a few lines of 
straightforward API calls that first retrieve data from a source, output the `clean_data`
dictionary and plot the data on a figure. While internally this involves sophisticated
data retrieval & processing methods, extensive manipulations & calculations, and
intricate plotting routines, this process can be completed by the user in just two lines
of code for most integrated data sources. The simplicity of these "tools" in SounderPy's 
"toolbox" allows quick and easy use for researchers, students, and hobbyists alike. After 
importing the library, just two lines of code will create Figure 1. On top of the many
integrated data sources, SounderPy also allows users to utilize their own custom data. So 
long as a user's custom data can be manually sorted into a `clean_data` dictionary, it can
be used with SounderPy's analysis and plotting functionality. 




![Figure 1: A sounding figure of NCEP RAP reanalysis data for a severe weather event in northern South Dakota on August 28th, 2024](figure_1.jpg)

# Acknowledgements

The development of SounderPy relies on the robust functionality provided by
several foundational Python libraries, including MetPy [@metpy], NumPy [@numpy], Matplotlib [@matplotlib],
xarray [@xarray], Cartopy [@cartopy], SHARPpy [@sharppy], SciPy [@scipy], and others. SounderPy gratefully acknowledges the
valuable contributions of individuals who have enhanced this project, including
Scott Thomas (National Weather Service), Daryl Herzmann (Iowa State University),
Amelia R.H. Urquhart (University of Oklahoma), Ryan Vandersmith, and many others. [@Elements.2016]

This project also extends its graditude to the researchers, institutions, and 
individuals who have utilized SounderPy in their work and publications, driving
its growth and application within the meteorological community.

# References
