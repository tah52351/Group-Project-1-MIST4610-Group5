# Group 5 Mist 4610 Project 1

# Team Name:

39217 Group 5

# Team Members:

1. Becca Paden @
2. Charlotte Moore @
3. Gabe Hanes @
4. Tyler Haleblian @
5. Logan Carras @

# Problem Description:

!!!

# Data Model

Explanation of data model:

The database is well-suited for managing clothing e-commerce orders and tracking the specific clothes customers buy, when they buy them, and how those products are categorized. Like a real clothing store, the database maintains basic information from each customer in order to maintain a clientele record. It also keeps track of the orders from each customer, when it was ordered, where it is going to, and to what customer it is being sent to. 

In real clothing stores, every time a customer orders there will be an address, order date, and an order ID attached to a customer’s ID. This is shown in the database, and it is used to ensure successful delivery of the item. The database opens opportunities to sell a variety of clothing items that are specific in the name of the item, the price, size, color, and category (type). Categories (like Shirts, Hats, Dresses, Pants, etc) and subcategories (T-shirts, Long-sleeved shirts, tank tops, etc) are used to specify items for the consumer so they know exactly what they are ordering.


# Data Dictionary:

!!!

# Queries:

Screen Shot 2023-03-31 at 6 37 36 PM

Query 1 lists the number of reservations at each dining establishment that were made for between 6 and 8pm as well as the name of each dining establishment these reservation were made for. The results are also ordered by number of reservations in descending order.
Screen Shot 2023-03-31 at 5 50 12 PM

Query 1 allows allows managers to see which establishments have received the most number of reservations during their busiest time (6-8pm) which is typically dinner time. These establishments likely need more support, resources, and personnel around dinner time. Therefore, this query allows managers to identify which establishments to allocate this extra help to. Listing the results in descending order of number of reservations makes it easier to see which establishment to prioritize.

Query 2 lists the number of dining reservations made by guests on each floor. The results are ordered in ascending order of floor number.
Screen Shot 2023-03-31 at 5 50 39 PM

Query 2 allows managers to see whether there is a trend between what floor a guest stays on and how much they reserve tabes at the resort's dining establishments. If managers were to find that dining reservations decreased as the floor number increased, it would have possibly indicated that guests were not dining at dining establishments because they felt the distance of the dining establishment from their room was too far and inconvenient.

Query 3 lists the information for all the guests who have not made an activity reservation.
Screen Shot 2023-03-31 at 5 52 01 PM

Query 3 allows the resort to market toward specific customers and contact them (e.g. promotional emails/coupons) about must-try activities. This helps to maximize revenue and increase efficiency by specifically targeting those who are not engaging in activities, rather than wasting time and resources to advertise to those who are already aware of and partaking in these activities.

Query 4 lists the names and phone numbers of dining employees who work in the highest rated dining establishment.
Screen Shot 2023-03-31 at 5 53 30 PM

A restaurant with a high star rating is a large source of revenue for the resort and management may want to know the names of the employees who work there and how to contact them to reward them for maintaining such a high achieving restaurant (e.g. via a bonus, raise, awards, recognition) or to know which employees to target for continuous training and supervision in order to keep service within the establishment in top shape.

Query 5 lists the guests’ names and the hotel they are checking into if their reservation is during the PM, their room is a single or suite, their check in dates are between 2023-04-01 and 2023-04-10, and their hotel rating is above a 4.
Screen Shot 2023-03-31 at 5 54 41 PM

Query 5 allows the resort to manage how busy their check in will be during the PM hours of early April in their better hotels where the check in rooms are singles or suites. This can help the resort determine how many employees need to be working the check in desks to check in single or suite reservations in the afternoon of these dates in these specific hotels.

Query 6 lists the names of guests who have over 10 activity reservations and the activities that they have those reservations in.
Screen Shot 2023-03-31 at 5 55 37 PM

Query 6 allows the resort to determine what guests are contributing the most to each activity’s revenue. The resort may use this information to reward guests who spend the most on activities by offering special prizes and promotions, creating guest loyalty and creating an incentive to reserve even more.

Query 7 lists the the amount of dining reservations per guest and the average amount of guests these reservations have.
Screen Shot 2023-03-31 at 5 56 06 PM

Query 7 allows the resort to see how many guests they should plan to seat, how the tables should be set up, and can lead to the resort figuring out how much revenue should be expected for the average visit.

Query 8 lists the guestID, guest name, and the number of room reservations per guest.
Screen Shot 2023-03-31 at 6 34 05 PM

Query 8 allows the resort to identify their frequent customers and how many times they have stayed. This could lead to a card system down the line. If a guest reaches 5 or 10 visits, there could be a platinum card which would gift the user reservation priority, food discounts, and other perks.

Query 9 lists all the rooms along with their average room view rating if the rating is above a 4 star. Additionally, the query is sorted by the view rating and arranged in descending order.
Screen Shot 2023-03-31 at 5 56 31 PM

Query 9 allows the employees and customers to see which rooms have an average view rating of 4 or more. Rooms with extravagant views are huge attractions to customers and can be a deciding factor when picking which room to stay in. This will help employees find which rooms have the best views fast and efficiently when asked.

Query 10 lists the names and prices of all activities offered by the resort that have not yet been booked by any guests and that are less than or equal to $50. Additionally, the results of the query are ordered by price in ascending order.
Screen Shot 2023-03-31 at 5 57 00 PM

Query 10 allows the employees and customers to see what activities have not been booked yet, and the prices for these activities. The price is sorted in ascending order to make it easier to find the most affordable activities which most people are looking for. Activities are a huge part of the resort experience and using this script will make it easy for employees to find which activities are available as well as the prices for these activities.

Database information:

Name of the database: ns_21479_1

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q1();
