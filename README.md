# createDBCMD
This repository contains a text file which explains the process of creating a database with tables in command prompt using MySQL.
The repository also has screenshot images of the commands used to create the Database.


/// Command prompts for connecting to a Database using Xampp and using the Apche and MySQL modules. ///

Cd/
C:
cd xampp
cd mysql
cd bin
mysql -u root -p -h 127.0.0.1
Password : Enter (No password)
![connect to db 1](https://user-images.githubusercontent.com/33934161/43719204-60fa5bb0-998d-11e8-8106-8fe2878e9aae.png)


/// This command prompt is used to see available databases. ///
SHOW DATABASES;


/// We want to create a new database called movies. Prompt below.///

CREATE DATABASE movies;
USE movies; /// Going inside the database. ///
SHOW TABLES;

![creating db 2](https://user-images.githubusercontent.com/33934161/43719500-2770c6b2-998e-11e8-88eb-1259d9f724d4.png)

/// Creating a table within the database declaring field names and parameters. ///

CREATE TABLE store (

-> movie_id INT NOT NULL AUTO_INCREMENT,
-> movie_title VARCHAR(50) NOT NULL,
-> movie_released VARCHAR(50) NOT NULL,
-> movie_length INT(10) NOT NULL,
-> movie_lang VARCHAR(50) NOT NULL,
-> PRIMARY KEY ( movie_id )
-> );

![creating table 3](https://user-images.githubusercontent.com/33934161/43719907-5833d1e4-998f-11e8-9683-f2ffb3765cdd.png)

///Inserting data into the tables.///

INSERT INTO store (
-> movie_id, movie_title, movie_released, movie_length, movie_lang)
-> VALUES (1, "Titanic", 1997, 195, "English");


INSERT INTO store (
-> movie_id, movie_title, movie_released, movie_length, movie_lang)
-> VALUES (2, "BadBoys", 1997, 132, "English");

INSERT INTO store (
-> movie_id, movie_title, movie_released, movie_length, movie_lang)
-> VALUES (3, "Poena Is Koning", 2000, 150, "Afrikaans");

INSERT INTO store (
-> movie_id, movie_title, movie_released, movie_length, movie_lang)
-> VALUES (4, "Blue Streak", 1998, 102, "English");

INSERT INTO store (
-> movie_id, movie_title, movie_released, movie_length, movie_lang)
-> VALUES (5, "All About the Benjamins", 1995, 126, "English");

![insert db 4](https://user-images.githubusercontent.com/33934161/43721055-19ac1f6e-9992-11e8-96db-02c728d9bb76.png)

/// Updating a record in the table. In this case, we updated the year release of a movie. ///

UPDATE store
-> SET movie_released = 1999
-> WHERE movie_id = 2;

/// Here we are deleting a record of information about a movie. ///

DELETE FROM store WHERE movie_id = 1;
![update and delete db 5](https://user-images.githubusercontent.com/33934161/43721128-42d1a83c-9992-11e8-8236-5daa26b06ce2.png)
