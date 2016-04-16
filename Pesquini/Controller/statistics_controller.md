# Class EnterpriseController

## Methods

### index
    empty

### most_sanctioned_ranking
    Retrieves the ranking of enterprises by the number of sanctions.

### most_paymented_ranking
    Retrieves the top ten payments of an enterprise.

### enterprise_group_ranking
    Groups and retrieves enterprises by the number of sanctions.

### payment_group_ranking
    Groups and retrieves enterprises by the number of payments.

### sanction_by_state_graph
    Sets all params for the graph of an enterprise based on its state.

### sanction_by_type_graph
    Sets all params for the graph of an enterprise based on its sanctions.

### total_by_state
    Retrieves an array with the sanctions filtered by a state, in a specific year.

### total_by_type

## Variables

### @@STATES_LIST
    A list that stores all states.

### @@sanjana
    A list that stores the sanctions of all years.

### @@SANCTION_LIST_TYPE
    A list that stores all the types of sanctions

### enterprise_group_array
    Stores the most sanctioned enterprises ranked.

### @enterprise_group
    Stores the group of enterprises that are in ranking.


### @enterprise_group_coun
    Stores the number of sanction of each enterprise that are in ranking.

### @all
    Boolean varibale used to indicate that a condition of an if statement was true.

### @enterprises - most_paymented-ranking
    Stores the featured payments of enterprises.

### @quantidade
    Stores the quantity of sanctions of an enterprise.

### @enterprises - enterprise_group_ranking
    Stores some enterprises that have a specific quantity of sanctions

### @quantidade
    Stores the quantity of payments of an enterprise.

### @enterprises - enterprise_group_ranking
    Stores some enterprises that have a specific quantity of payments.

### titulo
    Contains the name of the graph.

### @chart
    Object that stores the graph.

### f
    Auxiliar variable used to sed configurations of graph.

### @states
    Receives a copy of the @@STATES_LIST variable.
