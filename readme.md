# MegaDB
> JSON Veritabanı

Örnek

```js
const ibidi = require("mega.db")
const db = new ibidi({
    "dbName": "test", // Dosta adı test
    "dbFolder": "database", // Klasör adı örn: ./database
    "noBlankData": true, // Boş veri kayıt edilsin mi?
    "readable": true, // Veriler okunabilsin mi?
    "language": "tr" // Dil seçenekleri; tr, en.
}) // database/test.json

db.set("x.y.z", "abc") // {"x": "y": "z": "abc"}

db.get("x") // {y: {z: "abc"}}
db.all() // {x: {y: {z: "abc"}}}

db.push("a", "hello") //  ["hello"]
db.push("a", "world") //  ["hello", "world"]
db.unpush("a", "hello") // ["world"]

db.push("b", {name: "MEGA"}) // "b": [ {name: "MEGA"} ]

db.push("b", {name: "Database"}) // "b": [{name: "MEGA"}, {name: "Database"}]


db.delete("x") // anaveriyi siler!
db.delete("x.y.z") // altveriyi siler!

db.deleteAll() // Herşeyi siler!

```

