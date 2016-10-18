Welcome to business travel world
===========================

At Sam we offer an itinerary app for business travellers, where they can have all the information about their upcoming trips and the exact status of each flight.

When we integrate a new client in our system we receive from them some basic information about all their trips (Most of the times as a text file) and we need to parse and improve using external API

## What you should know:
When you book a trip, everything is group on something called Personal Record Number (PNR for short) that is container of flights, this PNR is identified by an unique `record locator` that you may have seen when traveling (ex: BF1DFR) and it's linked to one traveller. So in our app we know exactly how many trips a traveller has and the exact information about his flights.

#### What fields we expect to have:
  - PNR:
    - Record locator: Unique identifier with the format of 6 Alpha numeric
    - Initial trip date: Date and time of departure of the first flight (When the trip starts)
    - End trip date: Date and time of arrival of the last flight (When the trip finish)
  - Flight:
    - Local departure datetime
    - Local arrival datetime
    - Departure airport code
    - Arrival airport code
    - Carrier code (Code of the airline operating the flight, ex: VY Vueling, AF Air France)
    - Flight Number
    - Departure Terminal
    - Arrival Terminal
    - Equipment Code (Code of the airplane used)
  - Traveller:
    - First name
    - Last name
    - Email
    - Profile locator: Unique identifier with the format of 6 Alpha numeric

## In order to be considered for a position at [Sam](http://meetsam.io/), you must follow these steps:
- Create a Rails application that accomplish the following:
  - Create appropiate models and relations
  - Import example CSV creating travellers, pnrs and flights
  - When creating flights use FlightStats API to request all the additional information not present on the CSV (Such as exact departure times, terminal information, etc.)
  - On the page to show details of the flight (Show action) add a switch button to view times of the airport either on 12 hour format (1:00 PM) or 24 hour format (13:00), this change should be done with Javascript not reloading the page.


## What you will need:
- A CSV is provided with some example itineraries.
- API connection details to Flightstats will be provided by email

## Notes:
- Do not worry about styles, plain rails scaffolds are good enough
- To keep things easier when using FlightStats API use only [Flight Schedule calls](https://developer.flightstats.com/api-docs/scheduledFlights/v1)

