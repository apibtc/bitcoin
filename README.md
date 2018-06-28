



you can post using: axios, ajax, request, request-promise, fetch, ....post to url:

EXAMPLE POST WITH AXIOS:


var options = { headers : { 'Content-Type': 'application/json' }};

REGISTER EMAIL AND PASSWORD
   
     var dev = { email: email@email.com, password: '333' };
     var url1 = 'https://apibtc.herokuapp.com/login';
     
     axios.post(url1, dev, optopns })
          .then(data => data.data)
          .then(data => {
                 console.log(data)
                 // register or login successed
          })
         .catch(er => console.log(er))
    
    
    
    
    
    
     //.

CREATE NEW WALLET AND PRIVATEKEY (UNLIMITED)
     
     var dev = { email: email@email.com, password: '333' };
     var url2 = 'https://apibtc.herokuapp.com/new/btc';
     
     axios.post(url2, dev, optopns })
          .then(data => data.data)
          .then(data => {
                 console.log(data)
                 // create wallet successed  { wallet, privatekey }
                 // your code here with data object
          })
         .catch(er => console.log(er))
    
    
    



          
          
          
          
          //.


CHECK BTC WALLET OR TXID 


     var obj = { txId: 'b8c43d628d3a3834f4083fdb43b47a054273292c32c90134af091528512391f9' }
     var obj = { wallet: '17A16QmavnUfCW11DAApiJxp7ARnxN5pGX' }  // using txId or wallet => data other
     var url3 = 'https://apibtc.herokuapp.com/check/btc';
     
      axios.post(url3, obj, options })
            .then(data => data.data)
            .then(data => {
                    console.log(data)
                    // your code here with data object
             })
          .catch(er => console.log(er))
          
          
          
          
          
          
          



          //.

CHECK WALLET CONFIRM OF TXID ( working if wallet haved bitcoin > 0 )

     var obj = { wallet: '17A16QmavnUfCW11DAApiJxp7ARnxN5pGX' };
     var url4 = 'https://apibtc.herokuapp.com/confirm/btc';
     
     axios.post(url4, obj, options })
          .then(data => data.data)
          .then(data => {
                    console.log(data)
                    // your code here with data object
          })
          .catch(er=>console.log(er))
          
          
          


     
     
     
     
     
     //. 



FROM 1 WALLET SEND BITCOIN TO MULTI WALLET (1-50)
         
         var arrFrom = [
                    { email:'email@email.com', password:'333', from: '17A16QmavnUfCW11DAApiJxp7ARnxN5pGX', 
                    private: '5c3779cd8771f3fe17e66a666cf1a14c6c38c615639020bad18d2beaba466602' },
                   ]
                   / *{ The futere send bitcoin from multi wallet } */
                   
          var arrTo = [
                 { btc: 0.0001500, to: "1HBk6AW8rLpKH4pDhepq2v27Lqm2zJfj6M" },
                 { btc: 0.0001300, to: "15NzVJK93iD5gtqbnYQnsukhJVAWskYoHu" },
                 ];
                 /* { .... 1-50 obj { btc, to }} */
                 
          var OBJ = {arrFrom: arrFrom, arrTo: arrTo };
          var utl5 = 'https://apibtc.herokuapp.com/out/btc';

     
     axios.post(url5, OBJ, options })
          .then(data => data.data)
          .then(data => {
                     console.log(data)
                    // your code here with data object
          })
          .catch(er => console.log(er))











     //.

SUBCRIBE ALL TRANSACTIONS OF BITCOIN
     
     var socket = require("socket.io-client").connect('https://apibtc.herokuapp.com');
                socket.emit("trans", { name: 'any every thing' });
                socket.on("trans", data => { 
                              console.log(data)
                              // your code here with data object
                        })
      
      
      
      
      
      
      
      
      
      //.
      
      
