# steel-data-
	Shubham runs a top end car showroom but his data analyst has just quit and left him without his crucial insights.
so,my work is to annalyze the data and get various information like cars,manufacturers etc
-Case study has three dataset which are cars,sales and salespersons.
![Screenshot (6)](https://github.com/prashant9621/steel-data-/assets/136049491/84b9fb7f-f5c3-4e12-b71c-f8de2b87d9fc)
-There are some question related to dataset like,
1-Details of all cars manufacturer in 2022?
select c.car_id,c.make,c.type,c.style,c.cost,s.purchase_date from sales s join cars c on c.car_id = s.car_id where year(s.purchase_date)=2022;
![Screenshot (7)](https://github.com/prashant9621/steel-data-/assets/136049491/06e0277a-9385-412a-bcc7-4d19447158d6)
2-What is the total number of carssold by each salespersons?
select sp.name,count(*) as total_cars_sold from salesperson sp join sales s on sp.salesman_id=s.salesman_id group by sp.name;
![Screenshot (8)](https://github.com/prashant9621/steel-data-/assets/136049491/06bdf6af-9f29-4867-811d-f67363dc1763)

select 
3-What is total revenue genarated by each salespersons?
select sp.name,sum(c.cost) as total_revenue from salesperson spjoin sales s on sp.salesman_id=s.salesman+id join cars c on c.car_id=c.car_id group by sp.name;

4-What is the total revenue generated by each car type ?
select sp.name,c(*) from saleperson sp join sales s on sp.salesman_id=s.s.salesman_id join cars c on s.car_id=c.car_id ;
5-what is the name and city of the salesperosn who sold the most number of cars i the year 2023 ?
select top1 sp.name as salespeson,sp.city,year(s.purchase_date) as year,count(car_id) as total_cars from salesperson sp join sales s onorer by total_cars desc;


conclusion-Tom lee is best salesperson of 2023 hence appreciation or bonus should be given so that it sets example among other salesperson
2-c-class ,x5 and coroolla generate most revenue hence putting effort to upgrade  this cars benefit bussisness.
3-lowest popular car type is A4, so,it is advisable to stop paying upon its maintenance.
