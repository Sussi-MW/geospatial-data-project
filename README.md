<img src="https://github.com/Sussi-MW/geospatial-data-project/blob/master/portada.jpg" width="1000" height="400">

# Project: GeoSpatial Data
## by Susana Martin Wanton

## Goal: Place the new company offices in the best place.

The objective of this project is
define the location of a property that will be used as offices of a new company in the `GAMING industry`.

The analysis of the location is based on a survey carried out with the employees, in which they indicated their preferences regarding the environment.

The possible location of the office is defined with the help of queries to a database that contains more than 18k documents from different companies around the world, and each of them has a lot of information about each of the companies.

In addition, to obtain data from the closest places of interest, an information search is carried out in the Foursquare API, a service based on web location applied to social networks.

---

## Procedure:

### Start up

```bash
1-(query the database.ipynb)
2-(analysis_of_data.ipynb)
```

### Location

### 1. Exploring the MongoDB dataset to select location

- Obtain all companies that have less than 100 employees and that have an Appraisal Amount greater than 1,000,000.

- Get all companies located in San Francisco that have at least 90 employees but fewer than 200. Excluding companies that have a value of None in the Offices / Latitude field.

In the data frame it is observed that San Francisco is the most repeated location

We choose 'hi5' as the first option

#### Get location

latitude = 37.788668
longitude = -122.400558

#### Visualization on  map

```bash
1(ubicación_seleccionada.html)
```

### 2. Study of nearby location requirements

####  2.1. Tech startups
Near successful tech startups that have raised at least 1 Million dollars

- Get all the businesses in San Francisco, founded after the year 2000, that have between 90 and 150 employees and that have raised at least 1 Million dollars. Excluding companies that have a value of None in the Offices / Latitude field.

#### 2.2. Starbucks
Executives like Starbucks A LOT

- Obtaining information from the Foursquare API, related to the Starbucks located within a radius of 500 m.

#### 2.3 Airport.
Account managers need to travel a lot

- Obtaining information from the Foursquare API, related to the Airport located within a radius of 230000 m.

#### 2.4 Nightlife Spot
Everyone in the company is between 25 and 40

- Obtaining information from the Foursquare API, related to the Night clubs located within a radius of 500 m.

#### 2.5 Vegan restaurants.
The CEO is vegan.

- Obtaining information from the Foursquare API, related to the Vegan restaurants located within a radius of 500 m.

#### 2.6 Daycare.
30% of the company staff have at least 1 child.

- Obtaining information from the Foursquare API, related to the Daycare located within a radius of 500 m.


### 3. General dataset with all points located

- Concatenation of all datasets

### 4. Visualization on  map

```bash
2(all_heat_map.html)
3(all_markers_map.html)
```

### 5. Analysis of data

Within a radius of 500m from the selected location, we have located the following sites:

- 16 Starbucks.
  Nearestt Starbucks: 37.788792 -122.400710 - dist 0.011923 miles

- 30 Nightlife Spot
  Nearestt Nightlife Spot: Atlas Tap Room 37.787880 -122.400027 - dist 0.061661 miles

- 14 Vegan restaurants
  Nearestt Vegan restaurants: Sunrise Deli 37.788611 -122.400532 - dist 0.004189 miles

- 3 Daycare
  Nearestt Daycare: Kids by the Bay - Financial District 37.785471 -122.398037 - dist 0.260106 miles

- The city has two airports.

- Also, very close to the office location are 10 successful tech startups.
  Nearestt tech startups: Twilio 37.789850 -122.400683 - 0.081800 miles

---
## Resources used

* [Python Functional Programming How To Documentation](https://docs.python.org/3.7/howto/functional.html]
* [Python Errors and Exceptions Documentation](https://docs.python.org/3/tutorial/errors.html]
* [StackOverflow String Operation Questions](https://stackoverflow.com/questions/tagged/string+python]
* [API][https://developers.google.com/places/web-service/search]
* [API][https://developer.foursquare.com/]
* [https://docs.mongodb.com/manual/geospatial-queries/]
* [https://data.crunchbase.com/docs]
* [https://cloud.google.com/maps-platform/places/]
* [https://www.meetup.com/meetup_api/]
