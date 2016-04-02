# Class comments-controller

    This class is responsible to manipulate everything about the routes that's are made by users.

## Methods

### index

    This method returns a variable called '@route' that contains a new object of the route. This method is called from the view package to show the web page to the user too.

### trace_route

    This method return the result of other method 'get_accidents_data_to_sinalize' and render the index of this part of the software. The variable '@route' receives a new object of route with another variable 'origin_params' in the parameter.
    '@origin_informed_by_user' Receives the origin specified from the object '@route'.
    The variable '@destination_informed_by_user' receives the destination of the object as '@origin_informed_by_user' do.

### get_accidents_data_to_sinalize

    In this method, the variable 'latitude' will receives the accident latitude, as like 'longitude' receives accident longitude and 'br' receives the highway thats the accident occurred.
    This method returns the method 'remove_unusable_coordinates' with latitude, longitude and 'br' with parameters.

### remove_unusable_coordinates

    This method receives three parameters 'latitude', 'longitude', 'br' and returns the call of the method 'send_accidents_data_to_js' giving three arrays in the parameters.
    In a while loop have to make a checking about the value of the latitude, after that the content of the array is inserted in another array.

### send_accidents_data_to_js

    This method have 'latitude', 'longitude' and 'br' as parameters. After that, all the variables are changed to java script mode.

### origin_params

    This method take the data from url to be used in this class. The data are 'origin' and 'destination' of the route.

## Variables

### @route

    This is a object of the class route.

### @orgin_informed_by_user

    This instance variable receives the origin of the route.

### @destination_informed_by_user

    This instance variable receives the destination of the route.

### latitude

    This variable receives the latitude of an accident.

### longitude

    This variable receives the longitude of an accident.

### br

    This variable receives the number of the highway of the accident.

### latitudeUsable [ ]

    This array content all the correct latitudes of the accidents.

### longitudeUsable [ ]

    This array content all the correct longitudes of the accidents.

### highways [ ]

    This array content all the correct number of the highways of the accidents.

## Attributes

    Empty.
