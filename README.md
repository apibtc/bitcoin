create new wallet bitcoin and privatekey:

post to: 
axios.post('https://apibtc.herokuapp.com/new/btc', {email:email@email.com, password:'password'}, {headers:{'Content-Type': 'application/json'}})
.then(data=>data.data)
.then(data=>{
console.log(data)
// your code hare with data object
})
.catch(er=>console.log(er))

\n\n\n\n\n\n
check transaction:
check wallet:
check confirm of wallet:
send bitcoin from 1 wallet to 1-99 wallet in 1 transaction
