CREATE DATABASE Chanpionship;

USE  Chanpionship;

CREATE TABLE Divisions (
ID int IDENTITY NOT NULL PRIMARY KEY,
DivisionName varchar(50)
);

CREATE TABLE Managers (
ID int IDENTITY NOT NULL PRIMARY KEY,
FirstName varchar (25),
LastName varchar (25),
);

CREATE TABLE Teams (
ID int IDENTITY NOT NULL PRIMARY KEY,
TeamName varchar(50), 
DivisionID int NOT NULL FOREIGN KEY REFERENCES Divisions(ID)
ManagersID int NOT NULL FOREIGN KEY REFERENCES Managers(ID)
);

CREATE TABLE FootballPlayers (
ID int IDENTITY NOT NULL PRIMARY KEY,
FirstName varchar (25),
LastName varchar (25),
TeamID int NOT NULL FOREIGN KEY REFERENCES Teams(ID)
);

CREATE TABLE Referees (
ID int IDENTITY NOT NULL PRIMARY KEY,
FirstName varchar (25),
LastName varchar (25)
);

CREATE TABLE Matches (
ID int IDENTITY NOT NULL PRIMARY KEY,
DivisionID int NOT NULL FOREIGN KEY REFERENCES Divisions(ID),
RefereeID int NOT NULL FOREIGN KEY REFERENCES Referees(ID),
HomeTeam varchar(50),
GuestTeam varchar(50),
HomeTeamScore int NOT NULL,
GuestTeamScore int NOT NULL,
MatchDate DATE NOT NULL
);

INSERT INTO Divisions (DivisionName)
VALUES ('First League');

INSERT INTO Divisions (DivisionName)
VALUES ('Second League');

INSERT INTO Divisions (DivisionName)
VALUES ('Third League');

INSERT INTO Managers (FirstName, LastName) Values ('Gheorghe', 'Hagi');
INSERT INTO Managers (FirstName, LastName) Values ('Diego', 'Alonso');
INSERT INTO Managers (FirstName, LastName) Values ('Christian', 'Streich');
INSERT INTO Managers (FirstName, LastName) Values ('Barak', 'Bakhar');
INSERT INTO Managers (FirstName, LastName) Values ('Guillermo', 'Almada');
INSERT INTO Managers (FirstName, LastName) Values ('Massimo', 'Carrera');
INSERT INTO Managers (FirstName, LastName) Values ('David', 'Wagner');
INSERT INTO Managers (FirstName, LastName) Values ('Marco', 'Silva');
INSERT INTO Managers (FirstName, LastName) Values ('Phillip', 'Cocu');
INSERT INTO Managers (FirstName, LastName) Values ('Michael', 'O'Neill');

INSERT INTO Managers (FirstName, LastName) Values ('Eduardo', 'Berizzo');
INSERT INTO Managers (FirstName, LastName) Values ('Eddie', 'Howe');
INSERT INTO Managers (FirstName, LastName) Values ('Brendan', 'Rodgers');
INSERT INTO Managers (FirstName, LastName) Values ('Kurban', 'Berdyev');
INSERT INTO Managers (FirstName, LastName) Values ('Senol', 'Gunes');
INSERT INTO Managers (FirstName, LastName) Values ('Thomas', 'Tuchel');
INSERT INTO Managers (FirstName, LastName) Values ('Rafa', 'Benitez');
INSERT INTO Managers (FirstName, LastName) Values ('Ernesto', 'Valverde');
INSERT INTO Managers (FirstName, LastName) Values ('Giovanni van', 'Bronckhorst');
INSERT INTO Managers (FirstName, LastName) Values ('Arsene', 'Wenger');

INSERT INTO Managers (FirstName, LastName) Values ('Jorge', 'Jesus');
INSERT INTO Managers (FirstName, LastName) Values ('Unai', 'Emery');
INSERT INTO Managers (FirstName, LastName) Values ('Rui', 'Vitoria');
INSERT INTO Managers (FirstName, LastName) Values ('Ralph', 'Hasenhuttl');
INSERT INTO Managers (FirstName, LastName) Values ('Luciano', 'Spalletti');
INSERT INTO Managers (FirstName, LastName) Values ('Eusebio', 'Di Francesco');
INSERT INTO Managers (FirstName, LastName) Values ('Luis', 'Enrique');
INSERT INTO Managers (FirstName, LastName) Values ('Jorge', 'Sampaoli');
INSERT INTO Managers (FirstName, LastName) Values ('Marcelino', 'Garcia ');
INSERT INTO Managers (FirstName, LastName) Values ('Gian Piero', 'Gasperini');


INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Steaua',1, 1);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Pachuca',1, 2);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Borussia Dortmund',1, 3);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Be er Sheva',1, 4);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Ecuadorian Barcelona',1, 5);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Spartak Moscow',1, 6);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Huddersfield',1, 7);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Watford',1, 8);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('PSV',1, 9);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Northern Ireland',1, 10);

INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Sevilla',2, 11);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Bournemouth',2, 12);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Celtic',2, 13);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Rubin Kazan',2, 14);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Besiktas',2, 15);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('TBC',2, 16);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Newcastle',2, 17);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Barcelona',2, 18);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Feyenoord',2, 19);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Arsenal',2, 20);

INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Lions',3, 21);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('PSG',3, 22);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Benfica',3, 23);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('RB Lipzig',3, 24);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Inter',3, 25);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Roma',3, 26);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('TBC',3, 27);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Argentina',3, 28);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('valencia',3, 29);
INSERT INTO Teams (TeamName, DivisionID, ManagerID) Values ('Atlanta',3, 30);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Ken', 'Anderson', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Marcus', 'Allen', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Tom', 'Brady', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Kevin', 'Carter', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('James', 'Farrior', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Dermontti', 'Dawson', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Henry', 'Ellard', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Willie', 'Brown', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Jim', 'Hart', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Carl', 'Eller', 1);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Darrel', 'Green', 1);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Aaron', 'Rodgers', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Mike', 'Singletary', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Rick', 'Volk', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Max', 'Unger', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Jimmy', 'Johnson', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Anthony', 'Munoz', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Orlando', 'Pace', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Willie', 'Roaf', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Mike', 'Quick', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Bruce', 'Smith', 2);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Mikel', 'Webster', 2);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Bob', 'Young', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Charles', 'Woodson', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Randy', 'White', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Marshal', 'Yanda', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Jeason', 'Peters', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Jeff', 'Zgonia', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Randy', 'Cross', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('John', 'Hadl', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Ted', 'Hendricks', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Marvin', 'Harrison', 3);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Donnie', 'Edwards', 3);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Tunch', 'Ilkin', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Joe', 'Greene', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Darrel', 'Faneca', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Roger', 'Craig', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Herb', 'Adderley', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Tony', 'Dorset', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('London', 'Fletcher', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Chris', 'Doleman', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Tony', 'Gonzales', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('LeRoy', 'Irvin', 4);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Ken', 'Iman', 4);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Brett', 'Favre', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Warrick', 'Dunn', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Tim', 'Irwin', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Antonio', 'Gates', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Michael', 'Irvin', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Brian', 'Dawkins', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Bob', 'Griece', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Drew', 'Bress', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Derrick', 'Broos', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Jarred', 'Allen', 5);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('Jahri', 'Evans', 5);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 6);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 7);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 8);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 9);

INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);
INSERT INTO FootballPlayers (FirtsName, LastName, TeamID) Values ('', '', 10);

INSERT INTO Referees (FirstName, Lastname) VALUES ('Alexandre','Boucaut');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Johnaton','Lardot');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Luca','Banti');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Marco','Guida');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Carlos','Grande');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Mateu','Antonio');
INSERT INTO Referees (FirstName, Lastname) VALUES ('David','Borbalan');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Dacota','Wilson');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Antello','Alberto');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Jose','Jordan');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Raul','Orosco');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Guizadel','Ariel');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Balino','Ignacio');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Pitana','Nestor');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Fernando','Rapallini');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Silvio','Trucco');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Diego','Bonfa');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Julio','Fernandez');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Alfredo','Chade');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Virak','Khuon');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Karim','Abed');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Amaury','Delerue');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Nicolas','Reinville');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Frank','Shneider');
INSERT INTO Referees (FirstName, Lastname) VALUES ('Turpin','Clement');


INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)  
             Values ('2', 'Sevilla', 'Newcastlle', '1', '2', 1, '2018-08-20');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Setua', 'Be er Sheeva', '1', '1', '2', '2018-02-15');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'Atlanta', 'Roma', '3', '2', '3', '2017-12-02');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Spartak Moscow', 'PSV', '1', '2', '4', '2018-03-25');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Arsenal', 'Rubin Kazan', '0', '1', '5', '2016-07-05');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'Valencia', 'Argentina', '3', '1', '6', '2018-04-05');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Feyenoord', 'Besitkas', '1', '1', '7', '2016-09-04');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'Roma', 'Lions', '2', '0', '8', '2015-07-26');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'RB Lipzig', 'Inter', '0', '2', '9', '2018-05-29');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Pachuca', 'Celtic', '3', '3', '10', '2017-04-27');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Bournemouth', 'TBC', '1', '1', '11', '2018-06-17');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Arsenal', 'Barcelona', '0', '3', '12', '2018-08-30');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Borussia Dortmund', 'Nothern Ireland', '0', '0', '13', '2018-03-16');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'Benfica', 'Argentina', '2', '1', '14', '2017-06-19');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Huddersfield', 'Be er Shaeva', '1', '3', '15', '2018-01-27');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Feyenoord', 'Besitkas', '1', '1', '16', '2016-10-13');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Ecuadorian Barcelona', 'Setua', '2', '1', '17', '2018-10-18');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'Valencia', 'Atlanta', '1', '3', '18', '2018-10-10');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Nothern Ireland', 'Setua', '1', '1', '19', '2014-11-12');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Be er Sheeva', 'PSV', '2', '0', '20', '2017-06-22');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Rubin Kazan', 'TBC', '2', '3', '21', '2018-08-09');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('2', 'Barcelona', 'Newcastle', '4', '1', '22', '2017-03-15');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('3', 'Inter', 'Roma', '1', '0', '23', '2018-03-09');
INSERT INTO Matches (DivisionID, HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore, RefereeID, MatchDate)
             Values ('1', 'Waterford', 'Spartak Moscow', '1', '4', '24', '2015-05-23');



SELECT FirsName, LastName
FROM FootballPlayers
Where TeamID = 1; 
GO

SELECT HomeTeam, GuestTeam, HomeTeamScore, GuestTeamScore
FROM Matches
Where HomeTeam = 'Sevilla' OR GuestTeam = 'Sevilla';
GO


SELECT HomeTeam, GuestTeam, MatchDate
FROM Matches
Where HomeTeam = 'Sevilla' OR GuestTeam = 'Sevilla';
ORDER BY DATE;
GO



