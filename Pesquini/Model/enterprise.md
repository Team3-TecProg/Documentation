# Class Enterprise

## Methods

### last_sanction
    finds and returns a specific sanction object.
### last_payment
    finds and returns a specific payment object.
### payment_after_sanction?
    verifies that the initial date of sanction is greather than sign date of payment.
### refresh!
    returns an enterprise recovered by its cnpj.
### enterprise_position
    returns the index of an specific enterprise.
### most_sanctioned_ranking
    returns a variable with the enterprises sorted and grouped.

## Variables

### sanction
    auxiliar variable used to store the last sanction object.
### s
    variable that helps during iteration within elements of sanctions variable.
### payment
    variable used to store the last sanction object.
### payments
    variable that stores all the payments associated to an enterprise.
### f
    auxiliar variable that helps during iteration within elements of payments variable.
### e
    return of a function that finds an enterprise by its cnpj.
### orderedSanc
    stores the value of featured sanctions attribute.
### groupedSanc
    stores the value of orderedSanc organized by groups.
### k
    auxiliar variable that helps during iteration within elements of groupedSanc and b variables.
### index
    auxiliar variable that helps during iteration within elements of groupedSanc variable.
### enterprise_group
    stores all the first elements of each element in b.
### enterprise_group_count
    stores all the second elements of each element in b.
### enterprise_group_array
    stores the variables enterprise_group and enterprise_group_count.
### a
    stores all the enterprises sorted by the number of sanctions.
### b
    stores filtered elements of a, and groups them by number of sanctions.
### x
    auxiliar variable used to apply some action over some elements.

## Attributes

### string name
    stores the name of an enterprise.
### text description
    stores the description of an enterprise.
### text additional_info
    stores any possible additional information from a enterprise.
