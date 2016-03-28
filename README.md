# Converge lib

If you want to use the converge virtual merchant platform to handle your transactions. This library is a plug and play solution

https://www.convergepay.com/converge-webapp/developer/#/converge


## Usage

```js

var ConvergeLib = require('../index');
//pass your credentials
var convergeLib = new ConvergeLib(merchantId, userId, pin, testMode);


//Collect a payment
convergeLib.collectPayment('John','Johnson','info@customer.com','5114630000009791', '05', '17', '123',1.99 ,'1234','this is what i sold')
                .then(function(response){
                    console.log(response);
                })
                .catch(function(err){
                    console.error('error',err);
                    
                });
                
//Verify a card
 convergeLib.verifyCard('374101000000608', '05', '17', '123')
                .then(function(response){
                    console.log('response ',response);
                })
                .catch(function(err){
                    console.error('error',err);
                });

```

 