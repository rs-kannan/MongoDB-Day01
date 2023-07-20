# MongoDB-Day01
DATABASE NAME: Product_Deatils
COLLECTION NAME: products

1.Find all the information about each products
Ans: db.products.find()

2.Find the product price which are between 400 to 800
Ans: db.products.find({product_price:{$gt:400,$lt:800}})

3.Find the product price which are not between 400 to 600
Ans: db.products.find({product_price:{$not:{$gt:400,$lt:800}}})
  
4.List the four product which are grater than 500 in price 
Ans: db.products.find({product_price:{$gt:500}}).limit(4)

5.Find the product name and product material of each products
Ans: db.products.find().projection({product_name:1,product_material:1})

6.Find the product with a row id of 10
Ans: db.products.find({id:"10"}) 

7.Find only the product name and product material
Ans: db.products.find().projection({product_name:1,product_material:1})

8.Find all products which contain the value of soft in product material
Ans: db.products.find({product_material:"Soft"})

9.Find products which contain product color indigo  and product price 84
Ans: db.products.find({product_color:"indigo",product_price:84})

10.Delete the products which product price value are same
Ans: db.products.deleteMany({ product_price: 36 })
