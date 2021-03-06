# Fighters

#### Base endpoint: http://localhost:3001/fighters

### Use this endpoint to get information about any fighter who has ever fought in the UFC.
### Unfortunately the data is not complete for every fighter, as it is not publically available.

## Get All Fighters

### To get all fights you can send a GET request to the endpoint, as shown below:

```sh
const fights = fetch('http://localhost:3001/fighters')
  .then(resp => resp.status >= 400 ? Promise.reject() : resp.json())
  .catch(err => console.log('Oops!'));
```

## Warning!

### We have information for every fighter who has fought in the UFC, so expect a large pay load!

## Get A Fighter By ID

### To get a fighter you can send a GET request as shown below:

```sh
const fights = fetch('http://localhost:3001/fighters/:id')
  .then(resp => resp.status >= 400 ? Promise.reject() : resp.json())
  .catch(err => console.log('Oops!'));
```

### The response might look something like this:

```sh
{
  id: 12,
  name: "Juan Adams",
  nickname: "The Kraken",
  height: "6'5"",
  weight_lbs: "265",
  reach: "80"",
  stance: "Orthodox",
  dob: "Jan16,1992",
  wins: "5",
  losses: "3",
  no_contest: "0",
  record: "5-3-0",
  is_champ: false,
  slpm: "7.09",
  str_acc: "55%",
  sapm: "4.06",
  str_def: "34%",
  td_avg: "0.91",
  td_def: "57%",
  td_acc: "66%",
  sub_avg: "0.00",
  divisionId: 11,
  fights: [],
  potn: []
}
```