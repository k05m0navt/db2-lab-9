# Lab 9

## Daniil Gubajdullin

[ToC]

---

### Query 1

* Query: db.Restaurants.find(undefined)
* Output: output_1.json

---

### Query 2

* Query: db.Restaurants.find(undefined,{grades: 0,address: 0})
* Output: output_2.json

---

### Query 3

* Query: db.Restaurants.find({borough: 'Bronx'}).limit(5)
* Output: output_3.json

---

### Query 4

* Query: db.Restaurants.find({$or: [{ $and: [ { cuisine: { $not:RegExp('American') } }, { cuisine: { $not: RegExp('Chinees') } } ]},{name: { $regex: '^Wil' }}]},{grades: 0,address: 0})
* Output: output_4.json

---

### Query 5

* Query: db.Restaurants.find({name: {$regex: 'mon'}},{'address.street': 0,'address.building': 0,'address.zipcode': 0,grades: 0,restaurant_id: 0})
* Output: output_5.json

---

### Query 6

* Query: db.Restaurants.find({$or: [{ borough: 'Staten Island'},{ borough: 'Queens'},{ borough: 'Bronx'},{ borough: 'Brooklyn'}]},{grades: 0,address: 0})
* Output: output_6.json
