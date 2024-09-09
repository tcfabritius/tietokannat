### Tehtävä 1
select max(elevation_ft) from airport;
![ruudunkaappaus](kooste1.png)

### Tehtävä 2
select continent, count(*) from country group by continent;
![ruudunkaappaus](kooste2.png)

### Tehtävä 3
select screen_name, (select count(*) from goal_reached where game.id = game_id) from game;
![ruudunkaappaus](kooste3.png)

### Tehtävä 4
select screen_name from game where id in(select id from game where co2_consumed = (select min(co2
_consumed) from game));
![ruudunkaappaus](kooste4.png)

### Tehtävä 5
select name, (select count(*) from airport where airport.iso_country = country.iso_country) as count from country order by count desc;
![ruudunkaappaus](kooste5.png)

### Tehtävä 6
select country.name from country, airport where country.iso_country = airport.iso_country group by airport.iso_country having count(*) >= 1000;
![ruudunkaappaus](kooste6.png)

### Tehtävä 7
select name from airport where id = (select id from airport where elevation_ft = (select max(elevation_ft) from airport));
![ruudunkaappaus](kooste7.png)

### Tehtävä 8
select name from country where iso_country=(select iso_country from airport where id = (select id from airport where elevation_ft = (select max(elevation_ft) from airport)));
![ruudunkaappaus](kooste8.png)

### Tehtävä 9
select count(*) from goal_reached where game_id=(select id from game where screen_name="Vesa");
![ruudunkaappaus](kooste9.png)

### Tehtävä 10
select country.name from goal, goal_reached, game, airport, country where goal_reached.game_id = game.id and airport.iso_country = country.iso_country and goal_reached.goal_id = goal.id and game.location = airport.ident and goal.name = "clouds" and game.screen_name = "Ilkka";
![ruudunkaappaus](kooste10.png)