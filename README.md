# MongoDB Task

Here, I get a json from "https://github.com/rvsp/database/blob/master/mongodb/product.json" and write the query for the following questions.

Q1. Find all the information about each products
Solution: db.products.find({})

Q2. Find the product price which are between 400 to 800
Solution: db.products.find({product_price:{$gt:400,$lt:800}})

Q3. Find the product price which are not between 400 to 600
Solution: db.products.find({product_price:{$not:{$gt:400,$lt:800}}})

Q4: List the four product which are greater than 500 in price
Solution: db.products.find({product_price:{$gt:500}}).limit(4)

Q5: Find the product name and product material of each products
Solution: db.products.find({},{product_name:1,product_material:1})

Q6: Find the product with a row id of 10
Solution: db.products.findOne({"id":"10"})

Q7. Find only the product name and product material
Solution: db.products.find({},{product_name:1,product_material:1,_id:0})

Q8. Find all products which contain the value of soft in product material
Solution: db.products.find({product_material:"Soft"})

Q9. Find products which contain product color indigo  and product price 492.00
Solution: db.products.find({"product_color": "indigo", "product_price": 492.00})

Q10. Delete the products which product price value are 28
Solution: db.products.deleteOne({"product_price":28})





