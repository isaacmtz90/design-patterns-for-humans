💡 The Brief
--------

You are building a software for a parking lot. 
The parking lot will register every car thet comes into the parking lot, and charge when they leave.

Currently, our system supports cars and buses.
A car uses one parking lot, and a bus uses 3.
A car has to pay $3, and a bus $5.


We have a couple of new requirements: 

- The system should be able to to park Motorcycles (1/2 parking lot, $2 payment) and helicopters(5 parking lots, $30 payment).
- We are also giving a 50% discount if a car is electric. 

Our current solution looks something like this:
```
park(){
  if(type==='car'){
    return 1;
  }else{
    return 3;
  }
}
...

pay(){
  if (type ==='car'){
    return 3;
  }else{//is a bus
    return 5;
  }
}
```

It is obviously not compliant with the open-closed principle. We might also add new types of vehicles in the future.




Validation
--------
Some expected outputs are: 

- If a 3 cars and a bus come into the parking lot, we'll charge a total of $14 and the occupied parking lots would be 6

- If a bus and a helicopter come in, we'll charge $35, and use a total of 8 parking lots.
