# Background of the project

This project was completed as the final year project at Kathmandu University.
This project aims at creating TEC maps both in visualization and IONEX files.
Detailed report explaining the theoritical aspect of the project is also available
in this repo.

If any query, suggestion or any word regarding this project feel free to contact me
at binabhdevkota@gmail.com

# Getting Started and usage

## Requirements

* Python 3.x
* Continuous good internet connection

## Libraries to be installed

* Georinex
`pip install georinex`
* pymap3d
`pip install pymap3d`
* matplotlib
`pip install matplotlib`
* scipy
`pip install scipy`
* tkcalender
`pip install tkcalendar`
* wget
`pip install wget`
* unzlw
`pip install git+https://github.com/umeat/unlzw.git`
Make sure that you have **git installed and added to your path.** It can be downloaded from the [GIT website](https://git-scm.com/downloads "GIT website").
* pandas
`pip install pandas`

## Running the tool

After fulfilling all the requirements and installing all the required libraries you need to run the **main.py** script and the tool should start guving you the interface as shown in the screen captures then you are good to go.
The tool automatically downloads given the date and the stations. The data is downloaded from the
[UNAVCO Website](http://www.unavco.org "UNAVCO website"). Also for monthly DCB values of satellite Bias is downloaded from CODE's website. The data policy for data usage from UNAVCO is available [here](https://www.unavco.org/community/policies_forms/data-policy/data-policy.html "UNAVCO data usage policy") and data usage policy for data from CODE's website can be found [here](https://www.unibe.ch/legal_notice/index_eng.html "CODE data usage policy"). Users of this tool are requested to hava a look throughly and make sure to be aware about them. To know about exactly the data that was downloaded the data files can be found in the path `./data/<Year>/<dayofyear>`.

After downloading processing is done to generate TEC values for given time frame and given interval. After the processing is done one can easity generate the TEC maps. The generated TEC maps are in the form of matplotlib animation and IONEX file. The IONEX file is stored in `./data/<Year>/<dayofyear>` as .xxi file. it is also the location where all other data for that particular day are stored.

## Things to consider

There can be problems in the tool due to following reasons:

* Internet is not available.
* There is old data in the directory.
* If animation is not working while using spyder or Ipython IDE then please consider looking [here](https://stackoverflow.com/questions/35856079/animation-from-matplotlib-not-working-in-spyder "Stack Overflow") for solution. This might help. We are working more easy solutions.

In these cases try re-running the tool with good internet connection and clearing all previous data if generating TEC map for same day is giving problems.
