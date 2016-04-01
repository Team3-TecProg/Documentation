# Class highway-controller

## Methods

### index
	Receives a highway informed by the user, checks if it exists in the database, clean any ‘0’s on the left of its name, and holds it in a variable.
### setup_highway (highway)
	Sets up the result of the search_for_highway method to the @highway variable. Receives a highway parameter.
### check_length_and_if_exists (highway_to_check)
	Checks the length of the highway informed by the user, and then checks if it exists on the database. Receives a highway_to_check parameter.
### search_for_highway (highway_to_search)
	Searches for the highway informed by the user in the database. Receives a highway_to_search parameter.
### check_highway_number_length (highway_number)
	Checks if the length of the highway informed by the user is lesser than the MAX_HIGHWAY_NUMBER_LENGTH constant. Receives a highway_number parameter.
### check_highway_exists (highway_to_check)
	Checks if the highway informed by the user exists in the database. Receives a highway_to_check parameter.
### check_highway_number (highway_number)
	Receives the highway name and cleans it of any ‘0’s on its left. Receives a highway_number parameter.
### count_accidents_by_highway
	Saves the amount of Accident model objects in an @accident variable.
### order_accidents_by_accidentsRate
	Order the highways by their accident rates in reverse order (higher accident rates first), saves them in the @highway variable and calls the create_position method to rank them.
### calculate_accidentsRate (accidents_number, mileage_highway)
	Calculates the accident rate of a highway by dividing its accidents number by its mileage. Receives the accidents_number and the mileage_highway parameters.
### find_highway_to_accident
	Saves the accidents rate of a highway in its respective highway object, provided there was an accident there.
### create_position
	Saves the position of a highway in a raking, based on their accident rates.
### ranking_1
	Saves all the highways on the database in a variable and calls the find_highway_to_accident method.
### calculate_accidentsRatePercent (accidents_number, total_accidents)
	Calculates the percentage of accidents based on the accidents number on a hiven highway and the total of accidents registered. Receives the accidents_number and the total_accidents parameters.
### order_accidents_by_accidentsRatePercent
	Saves all the highways in the database ordered by their accident rates in a variable.
### ranking_2
	Saves all the highways from the database in a variable, all the accidents from the database in another variable, and calls the find_highway_to_accident_percent method.
### find_highway_to_accident_percent
	Saves the accidents percente rate of a highway in its respective highway object, provided there was at least one accident there.
### show
	Shows a given Highway model object in its HTML view page.
	
## Constants

### MAX_HIGHWAY_NUMBER_LENGTH
	Represents the maximum length permitted to a highway name.

## Variables

### @highway_informed_by_user
	Represents the highway name informed by the user.
### @highway_number_exists
	Holds True if the highway number informed by the user exists in the database, or False otherwise.
### cleaned_highway_to_check
	Represents the highway name informed by the user, but without any ‘0’s on the left.
### length_is_ok
	Holds True if the length of the highway informed by the user is lesser than the value of the MAX_HIGHWAY_NUMBER_LENGTH constant. Holds False otherwise.
### @highway
	Represents the highway from the database that matches the highway informed the user.
### highway_cleaned
	Represents the highway name informed by the user, but without any ‘0’s on the left (same as cleaned_highway_to_check).
### highway_number_length
	Holds the length of the highway informed by the user’s name string.	
### @accident
	Represents the amount of Accident model objects.
### rate
	Represents the rate of accidents of a highway.
### br_accident
	Represents the name of a BR in which there was an accident.
### count_accident
	Represents the number of accidents of a given highway.
### mileage_br
	Represents the mileage of a brazilian highway.
### @highways
	Represents all the highways in the database.
### accidents_number
	Represents the number of accidents on a highway.
### total_accidents
	Represents the number of registered accidents.
### @highway2
	Represents all the highways in the database ordered by their accident rate.
### @highways2
	Represents all the highways in the database.
### @accidents2
	Represents all the accidents in the database.
### @comment
	Represents a new Comment model object.
### @comments
	Represents existing comments related to a given highway.
