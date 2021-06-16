## Flyline_Ruby



Client library for talking to [Flyline API](https://flyline.io/docs/). Supports all endpoints, as well as travelling API requests

### How to Install

```sh
gem "flyline", :git => "git://github.com/FlyLine-Development/flyline_ruby.git"
```

### Usage

First of all, initialize client:

```ruby
client = Flyline::Client.new("FToken")
```



And then send Request according to your Request:

```ruby
client.get_seatTypes()
```

### List of All EndPoints

Client methods really just map 1 to 1 to API, see all of them beyond. Check [the API docs](https://flyline.io/api-ref) for list of available `data`.

```ruby
# getSeatList()
client.getSeatTypes();
# getLayoutList()
client.getSeatLayouts();
# getFoodList()
client.getFoods();
# getBeverageList()
client.getBeverages();
# getEntertainmentList()
client.getEntertainments();
# getWifiList()
client.getWifis();
# getPowerList()
client.getPowers()
# getAircraftList()
client.getAircrafts();
# getAirCraftByIataCode()
client.getAircraft(iata_code);
# getAirlineList()
client.getAirlines();
# getAirlineByIataCode()
client.getAirline(iata_code);
# getAirportList()
client.getAirports();
# getAirportByIataCode()
client.getAirport(iata_code);
# getAirportByCity()
client.getAirportsByCity(iata_code);
# getCityList()
client.getCities();
# getCityByIataCode()
client.getCity(iata_code);
# getCabinMapping()
client.getCabinClassMapping(carrier = optional, cabin_class = optional);
# getSeatMap({"carrier": "AA","aircraft": "738"})
client.getSeatMap(data);
# getSchedulesByFlightNumber({"airline": "AA","date": "2021-06-06","flight_number": "1105"})
client.getSchedulesByFlightNumber(data);
# getSchdulesByRoute({"origin": "JFK","destination": "DFW","airline": "AA","date": "2021-06-06"})
client.getSchedulesByRoute(data);
# getAirAttributesByFlightNumber({"cabin_class": "economy","departure": "DFW","arrival": "LAX","departure_date": "2021-06-15","flight_no": "2812","carrier": "AA"})
client.getAirAttributesByFlightNumber(data);
# getAirAttributeByRoute({"cabin_class": "economy","slices": [{"departure": {"code": "DFW","date": "2021-06-15"},"arrival": {"code": "LAX"}}],"passengers": 1})
client.getAirAttributesByRoute(data);
# getAirfares({"cabin_class": "economy","slices": [{"departure": {"code": "DFW","date": "2021-06-15"},"arrival": {"code": "LAX"}}],"passengers": 1})
client.getAirfares(data);
```
