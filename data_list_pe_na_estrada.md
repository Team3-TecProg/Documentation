# pe-na-estrada
---------------------------------------------------------------------------------------------

## Class accident

### Methods

* self.count_accidents
* self.total_accidents
* self.get_accidents_latitude
* self.get_accidents_longitude
* self.get_accidents_br

### Variables

* uf
* km
* br
* latitude
* longitude


------------------------------------------------------------------------------------------------------------------------

## Class comment

### Methods
	self.getComments

### Variables
	title
	text
	idBr

------------------------------------------------------------------------------------------------------------------------
## Class highway

### Methods
	self.search_for_highway (id_to_search)
	self.exists_highway (highway_to_chech)
	self.all_highways_by_accidentsRate
	self.all_highways_by_accidentsRateParcent
### Variables
	idBr
	mileage
	comments
------------------------------------------------------------------------------------------------------------------------

## Class route

### Methods
	self.getComments

### Variables
	origin
	destination
	address
	geocode
------------------------------------------------------------------------------------------------------------------------

## Class accidents_controller

	Empty.

------------------------------------------------------------------------------------------------------------------------

## Class comments-controller

### Methods
index
Generates an object of the Comment model and saves it in the  @comment variable.
create
Generates an object of the Highway model and saves it in the @highway variable.
Tries to save the comment created in the index method and redirects, if successful, to the highway path route.
comment_params
Fetches the parameters required by a comment object.
### Variables
 @comment
Represents an object of the Comment model.
 @highway
Represents an object of the Highway model.
Attributes
highway_id
Represents the id of a Highway model object.
title
Represents the title of a Comment model object
text
Represents the text body of a Comment model object
idBr
Represents the name of a brazilian highway, called BRs.



------------------------------------------------------------------------------------------------------------------------

## Class highway-controller

### Methods
index
Receives a highway informed by the user, checks if it exists in the database, clean any ‘0’s on the left of its name, and holds it in a variable.
setup_highway (highway)
Sets up the result of the search_for_highway method to the @highway variable. Receives a highway parameter.
check_length_and_if_exists (highway_to_check)
Checks the length of the highway informed by the user, and then checks if it exists on the database. Receives a highway_to_check parameter.
search_for_highway (highway_to_search)
Searches for the highway informed by the user in the database. Receives a highway_to_search parameter.
check_highway_number_length (highway_number)
Checks if the length of the highway informed by the user is lesser than the MAX_HIGHWAY_NUMBER_LENGTH constant. Receives a highway_number parameter.
check_highway_exists (highway_to_check)
Checks if the highway informed by the user exists in the database. Receives a highway_to_check parameter.
check_highway_number (highway_number)
Receives the highway name and cleans it of any ‘0’s on its left. Receives a highway_number parameter.
count_accidents_by_highway
Saves the amount of Accident model objects in an @accident variable.
order_accidents_by_accidentsRate
Order the highways by their accident rates in reverse order (higher accident rates first), saves them in the @highway variable and calls the create_position method to rank them.
calculate_accidentsRate (accidents_number, mileage_highway)
Calculates the accident rate of a highway by dividing its accidents number by its mileage. Receives the accidents_number and the mileage_highway parameters.
find_highway_to_accident

create_position
ranking_1
calculate_accidentsRatePercent (accidents_number, total_accidents)
order_accidents_by_accidentsRatePercent
ranking_2
find_highway_to_accident_percent
show
Constants
MAX_HIGHWAY_NUMBER_LENGTH
Represents the maximum length permitted to a highway name.
### Variables
@highway_informed_by_user
Represents the highway name informed by the user.
@highway_number_exists
 Holds True if the highway number informed by the user exists in the database, or False otherwise.
cleaned_highway_to_check
Represents the highway name informed by the user, but without any ‘0’s on the left.
length_is_ok
Holds True if the length of the highway informed by the user is lesser than the value of the MAX_HIGHWAY_NUMBER_LENGTH constant. Holds False otherwise.
@highway
Represents the highway from the database that matches the highway informed the user.
highway_cleaned
Represents the highway name informed by the user, but without any ‘0’s on the left (same as cleaned_highway_to_check).
highway_number_length
Holds the length of the highway informed by the user’s name string.
@accident
Represents the amount of Accident model objects.
rate
Represents the rate of accidents of a highway.
br_accident

count_accident
mileage_br
@highways
@highway2
@highways2
@accidents2
@comment
@comments
Parameters
highway
highway_to_check
highway_to_search
highway_number
Attributes
highway_search
Id

 ------------------------------------------------------------------------------------------------------------------------
## Class HomeController

### Methods
Index
### Variables
@highway
--------------------------------------------------------------------------------------------------------------------------
## Class HomeController
### Methods
index
trace_route
get_accidents_data_to_sinalize
remove_unusable_coordinates (latitude, longitude, br)
send_accidents_data_to_js (latitude, longitude, br)
origin_params

### Variables
latitude
longitude
br
latitudeUsable
longitudeUsable
highways
gon.latitude
gon.longitude
gon.br
@route
@origin_informed_by_user
@destination_informed_by_user
