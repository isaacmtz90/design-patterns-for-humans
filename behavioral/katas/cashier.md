💡 The Brief
--------

You are building a software for a parking lot.
We'll start with the cashier module. The cashier is in charge of creating receipts when a car goes out of a parking lot.

Currently, our cashier supports generating receipts for cars and buses.
A car has to pay a fee of $3, and a bus $5.

We have a couple of new requirements: 

- The system should be able to to park Motorcycles ($2.5 payment) and limousines( $10 payment).

Our current Receipt solution looks something like this:
```
...

GetFee(){
  if (type === 'Car'){
    return 3;
  }else{ //is a bus
    return 5;
  }
}
```

It is obviously not compliant with the open-closed principle. We might also need to add new types of vehicles in the future.




Validation
--------
Some expected outputs are: 

- If a car is leaving the parking lot the parking lot, the cashier should generate a receipt with a Fee of $3

- If a bus is leaving the parking lot the parking lot, the cashier should generate a receipt with a Fee of $5

- If a motorcycle is leaving the parking lot the parking lot, the cashier should generate a receipt with a Fee of $2.5
