Booking for tatkal tickets gets over in couple of seconds every day. Suppose the server takes 0.5 milliseconds to carry out a booking and it can do only one booking at a time. Assume an implemention of a queue requestQueue which contains the request time of all bookings. So as rquest comes to the server it is enqueued in requestQueue and the server reads the time and then makes the booking. After server finishes booking, it dequeues the time.

Answer the questions given below.

Time(in milliseconds) of booking requests

[0.0, 0.8, 1.1, 1.4, 1.5, 2.0, 2.3, 2.3, 2.4, 2.5]

What is the maximum size the requestQueue will reach?

6
  correct 

What is the first time (in milliseconds) at which requestQueue reaches the maximum size?

2.5
  correct 
  
At time: -1.0
requestQueue :[]

At time: 0.0
requestQueue :[0.0]

At time: 0.5
requestQueue :[]

At time: 0.8
requestQueue :[0.8, 1.1]

At time: 1.3
requestQueue :[1.1]

At time: 1.4
requestQueue :[1.1, 1.4]

At time: 1.5
requestQueue :[1.1, 1.4, 1.5]

At time: 1.8
requestQueue :[1.4, 1.5]

At time: 2.0
requestQueue :[1.4, 1.5, 2.0]

At time: 2.3
requestQueue :[1.5, 2.0, 2.3, 2.3]

At time: 2.4
requestQueue :[1.5, 2.0, 2.3, 2.3, 2.4]

At time: 2.5
requestQueue :[1.5, 2.0, 2.3, 2.3, 2.4, 2.5]

At time: 2.8
requestQueue :[2.0, 2.3, 2.3, 2.4, 2.5]

At time: 3.3
requestQueue :[2.3, 2.3, 2.4, 2.5]

At time: 3.8
requestQueue :[2.3, 2.4, 2.5]

At time: 4.3
requestQueue :[2.4, 2.5]

At time: 4.8
requestQueue :[2.5]

At time: 5.3
requestQueue :[]
