Write mongo commands to do the following:

> You can refer to official [mongo documentation](https://www.mongodb.com/docs/)

> No need to write any code, just create a `.md` file that shows step-by-step what commands needs to be run on mongo shell.

> You can create a free mongo database on `MongoDB Atlas` or install MongoDB locally.

1.	Create 3 collections: Users, Products, Orders
2.	Insert 2 users:
```
{
  Name: ‘Test User 1’,
  Address: {
    Line1: 'XYZ',
    Line2: 'ABC',
    PinCode: '123456'
  },
  Phone: [‘+91-123456789’, ‘+91-987654321’]
},
{
  Name: ‘Test User 2’,
  Address: {
    Line1: 'ASD',
    Line2: 'DFG',
    PinCode: '456678'
  },
  Phone: [‘+91-423356356’, ‘+91-5678356323’]
}
```
3.	Insert 2 products into product collection:
```
{
  Name: 'iPhone13',
  UnitPrice: 80000,
},
{
  Name: 'iPhone14',
  UnitPrice: 100000,
}
```
4.	Insert 2 orders into orders collection:
```
{
  OrderId: 'O-123',
  UserId: <_id of 'Test User 1'>,
  Items: [
    {
      ProductId: <_id of iPhone13>,
      ProductName: 'iPhone13',
      Quantity: 5,
      UnitPrice: 80000,
      Total: 400000
    }
  ],
  Total: 400000
},
{
  OrderId: 'O-456',
  UserId: <_id of 'Test User 2'>,
  Items: [
    {
      ProductId: <_id of iPhone13>,
      ProductName: 'iPhone13',
      Quantity: 5,
      UnitPrice: 80000,
      Total: 400000
    },
    {
      ProductId: <_id of iPhone14>,
      ProductName: 'iPhone14',
      Quantity: 2,
      UnitPrice: 100000,
      Total: 200000
    }
  ],
  Total: 600000
}
```
5.	Write a mongo aggregation to find out how many pcs of each product was ordered: (It has to be a mongo aggregation itself, no JS loop)
```
[
  {
    Product: 'iPhone13',
    TotalSold: 10
  },
  {
    Product: 'iPhone14',
    TotalSold: 2
  }
]
```
6. Write a mongo aggregation to find out which user has placed the higest order by value: (It has to be a mongo aggregation itself, no JS loop)
```
{
  UserId: '<_id of user that has higest number of orders by value'
}
```
