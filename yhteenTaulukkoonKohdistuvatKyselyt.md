### Tehtävä 1
select * from goal;
![ruudunkaappaus](teht1.png)

### Tehtävä 2
SELECT name, type
FROM airport 
WHERE iso_country = 'FI';
![ruudunkaappaus](teht2.png)

### Tehtävä 3
select name from airport where iso_country = "FI" order by name;
![ruudunkaappaus](teht3.png)

### Tehtävä 4
select name, type from airport where iso_country = "FI" order by type, name;
![ruudunkaappaus](teht4.png)

### Tehtävä 5
select name from country where name like 'F%';
![ruudunkaappaus](teht5.png)

### Tehtävä 6
select name from country where name like '%F%';
![ruudunkaappaus](teht6.png)

### Tehtävä 7
select location from game where screen_name = "Vesa";
![ruudunkaappaus](teht7.png)

### Tehtävä 8
select co2_consumed from game where screen_name = "Ilkka";
![ruudunkaappaus](teht8.png)

### Tehtävä 9
select co2_budget from game where screen_name = "Ilkka";
![ruudunkaappaus](teht9.png)