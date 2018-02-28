1) db.createCollection('orders')

2) db.getCollection('orders').insert({
  orderDate: ISODate("02/03/2017),
  });


db.getCollection('orders').insert({
  orderDate: ISODate("04/04/2017"),
  });

db.getCollection('orders').insert({
  orderDate: ISODate("01/02/2017"),
  });

3) db.getCollection('orders').find({}).pretty()

4) db.getCollection('orders').find({orderDate: {$gt: new ISODate('2017-01-31')}});

5) db.getCollection('orders').update({orderDate: ISODate("2017-02-03T22:23:20.201Z")}, {$set: {orderTotal: 63}});

6) 