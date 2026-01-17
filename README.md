# Persona5-Wallpaper-Engine-Weather-Addon
An addon that provides real world weather synconisation to the Real time Persona 5 Tokyo Transition screen + Weather wallpaper for wallpaper engine (https://steamcommunity.com/sharedfiles/filedetails/?id=2955378002). This app has 6 weather states; Sunny, Heatwave, Rain, Torrential Rain, Cloudy and Snow. The requirements for Heatwave and Torrential rain can be adjusted in the apps code. The app also automaticallty creates a log, and deletes old logs after the total size taken up is 1 MB.

I don't plan on adding any additional functionality to this app, but if something is broken, let me know.

The code is a framework and requires the addition of a personal (but free) open weather API code and the adjustment of the directories in the files so that the programs can be run, instructions provided below. To have it operate on launch windows task scheduler is used.

##### Set up
1. Prerequisites
 <br> Before starting, ensure you have:
    <br>Python installed (Python 3.10+ recommended)
2. Download the Files and Place into your documents folder
3. Install Required Python Modules
     <br>Open Command Prompt in the project folder and run:
     <br> python -m pip install requests
4. Edit the Script Configuration
    <br> Open wallpaper_weather_app.txt and replace the openweather API key, city and countrycode at the top of the file . Also under the heading WEATHER FETCHING, within the code you must replace the 3 as well (all additions require enclosement by "quotes"). After doing this rename the script to a .py file
5. Edit the run.bats
     <br>Open both the silent and silent_test txt files and edit the file paths listed to lead to the python.exe, wallpaper_weather_app.py, and to the Persona5WeatherAddon folders path. Save and close, then rename both files to be .bat files.
6. Testing
     <br>Now if set up correctly with the wallpaper running, openign silent_test.bat will cause the wallpaper to cycle through the 6 weather states every 5 seconds. If that is done then activating the other silent.bat will cause it to sync to your real world weather,

###### Troubleshooting
1. Ensure all file paths are correctly altered
2. Ensure all addition of API, countrycode and city are surrounded by "quotes"
3. The commands in command.json are inteneded to work with wallpaper engine 64 bit in the standard location in the C:Drive. If you have it elsewhere or the 32 bit version you will have to edit the commands, see here (https://help.wallpaperengine.io/en/functionality/cli.html#open-playlist)
   
