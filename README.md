# HackerRank JOIN
Average Population of Each Continents

MS SQL server

Problem - Given the CITY and COUNTRY tables, query the names of all the continents (COUNTRY.Continent) and their respective average city populations (CITY.Population) rounded down to the nearest integer.

Note: CITY.CountryCode and COUNTRY.Code are matching key columns.

Input Format

The CITY and COUNTRY tables are described as follows: 
![image](https://user-images.githubusercontent.com/90959192/156125491-ac66613e-f743-4940-b19d-a0fbfc33ec00.png)

![image](https://user-images.githubusercontent.com/90959192/156125623-047967ae-ba40-427c-8064-78cb1d88b7e2.png)


=======================================================================
Solution - 



select COUNTRY.Continent,FLOOR(avg(CITY.Population)) from COUNTRY inner join CITY
            ON CITY.CountryCode = COUNTRY.Code
            group by COUNTRY.Continent
           
========================================================================
