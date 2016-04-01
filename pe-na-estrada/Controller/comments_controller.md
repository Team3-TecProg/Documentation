# Class comments-controller

## Methods

### index
	Generates an object of the Comment model and saves it in the  @comment variable.
### create
	Generates an object of the Highway model and saves it in the @highway variable.
	Tries to save the comment created in the index method and redirects, if successful, to the highway path route.
### comment_params
	Fetches the parameters required by a comment object.

## Variables

### @comment
	Represents an object of the Comment model.
### @highway
	Represents an object of the Highway model.

## Attributes

### highway_id
	Represents the id of a Highway model object.
### title
	Represents the title of a Comment model object
### text
	Represents the text body of a Comment model object
### idBr
	Represents the name of a brazilian highway, called BRs.
