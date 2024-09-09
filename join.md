### Tehtävä 1
select country.name as "country name", airport.name as "airport name" from airport inner join country on airport.iso_country = country.iso_country where country.name = "Finland" and scheduled_service = "yes";
![ruudunkaappaus](join1.png)

### Tehtävä 2
select screen_name, airport.name from airport inner join game on airport.ident = game.location;
![ruudunkaappaus](join2.png)

### Tehtävä 3
select screen_name, country.name from game inner join airport on airport.ident = game.location inner join country on airport.iso_country = country.iso_country;
![ruudunkaappaus](join3.png)

### Tehtävä 4
select airport.name, game.screen_name from airport left join game on airport.ident = game.location where airport.name like "%Hels%";![ruudunkaappaus](join4.png)

### Tehtävä 5
select goal.name, screen_name from goal left join goal_reached on goal.id = goal_id left join game on game.id = game_id;
![ruudunkaappaus](join5.png)