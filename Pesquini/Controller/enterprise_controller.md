# Class EnterpriseController

## Methods

### index
    Searchs for a enterprise according the params sent by user, once did it, return a set of enterprises with pagination.

### show
    Sets the main params for exibition of enterprises, like quantity of enterprises by page and the entrepise's informations that should be showed.

### enterprise_payment_position
    Recover the index of a specific enterprise.

## Variables

### @search
    Stores a specific enterpise recovered for params sent by user.

### @enterprises
    Organizes enterprises with pagination according for params.

### @per_page
    Stores the value of 10, that means the maximum number of enterpises in one single page.

### @page_num
    Verifies if the param page is greater than zero.

### @enterpise
    Stores a enterpise found by its id.

### @collection
    Stores all the sanction that have a determinated enterprise_id.

### @payments
    Stores all the payment that have a determinated enterpise_id and organizes its by a style of pagination.

### @sanctions
    Organizes the sanctions stored on collection by a style of pagination.

### @payment_position
    Stores a index of a specific enterprise.

### @position
    Stores a index of a specific enterprise.

### p
    Used to iterate at each featured_payment in a Enterprise.

### a
    Auxiliar variable that helps during iteration, and stores each object in p.

### index
    Auxiliar variable that helps during iteration, and stores index of each object in p;
