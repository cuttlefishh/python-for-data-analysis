### Assignment 7 - Plotting

Complete the tasks below. Please turn in a single Jupyter notebook named `7_first_last.ipynb` (substitute your first and last name). Please run Kernel > Restart & Run All on your notebook before turning in.

#### Moons of the Solar System

For this assignment, we will collect and wrangle data about the moons orbiting planets in our Solar System, and then we will make some plots from those data.

**1.** Data collection and wrangling.

* Find an online resource with data about the moons and planets of the Solar System (sizes and distances).
* Create an Excel spreadsheet `moons.xlsx` with the following information about each moon (suggested column names shown): 
    - Moon name (`moon_name`)
    - Host planet name (`planet_name`)
    - Moon diameter in kilometers (`moon_diameter_km`)
    - Moon–planet distance in kilometers (`moon_planet_distance_km`)
* Create an Excel spreadsheet `planets.xlsx` with the following information about each planet (suggested column names shown): 
    - Planet name (`planet_name`)
    - Planet diameter in kilometers (`planet_diameter_km`)
    - Planet–Sun distance in kilometers (`planet_sun_distance_km`)

**2.** Comparing moon diameters and volumes to their host planets.

* Import `moons.xlsx` and `planets.xlsx` as Pandas DataFrames using `pd.from_excel()`.
* Merge the DataFrames using the planet names (hint: set `left_on=planet_name` and `right_on=planet_name`).
* Calculate the volume of each moon and planet; add these to your DataFrame (suggested column names: `moon_volume_km3`, `planet_volume_km3`). (Reminder: Volume = 4/3 * π * (Diameter/2)**3.)
* Plot moon diameter versus host planet diameter (i.e., x-axis = `planet_diameter_km`, y-axis = `moon_diameter_km`) and label each moon next to its corresponding marker. Save this plot as a PDF image.
* Plot moon volume versus host planet volume (i.e., x-axis = `planet_volume_km3`, y-axis = `moon_volume_km3`) and label each moon next to its corresponding marker. Save this plot as a PDF image.
* Optional: Go back to the plots and resize the markers so they are proportional to moon diameter.

**3.** Comparing moon and sun angular diameters.

* Calculate the angular diameter of each moon as if you were standing on the surface of its home planet; add these to your DataFrame (suggested column name: `moon_angular_diameter_arcsec`). (Reminder: Angular diameter in arcseconds = 206265 * Diameter / Distance.)
* Calculate the angular diameter of the Sun as if you were standing on the surface of each home planet; add these to your DataFrame (suggested column name: `sun_angular_diameter_arcsec`).
* Plot moon angular diameter versus Sun angular diameter for each moon and label each moon next to its corresponding marker (i.e., x-axis = `sun_angular_diameter_arcsec`, y-axis = `moon_angular_diameter_arcsec`). Add a line corresponding to a 1:1 ratio. Save this plot as a PDF image.
