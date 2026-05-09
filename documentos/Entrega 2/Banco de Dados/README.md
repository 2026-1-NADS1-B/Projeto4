CREATE DATABASE messier;
USE messier;
CREATE TABLE Game (
ID_Game INT PRIMARY KEY AUTO_INCREMENT,
Nome_game VARCHAR(100) NOT NULL,
Faixa_etaria VARCHAR(20),
Status_game VARCHAR(30),
Tema_game VARCHAR(50)
);
CREATE TABLE Pacote (
ID_Pacote INT PRIMARY KEY AUTO_INCREMENT,
Nome_pacote VARCHAR(100) NOT NULL,
Preco_pacote DECIMAL(10,2) NOT NULL,
Limite_de_Acessos INT NOT NULL
);
CREATE TABLE Escola (
ID_Escola INT PRIMARY KEY AUTO_INCREMENT,
Nome_Escola VARCHAR(150) NOT NULL,
Cnpj_Escola VARCHAR(18) UNIQUE NOT NULL,
Status_do_Pacote VARCHAR(30),
ID_Pacote INT,
FOREIGN KEY (ID_Pacote) REFERENCES Pacote(ID_Pacote)
);

CREATE TABLE Acesso (
id_acesso INT PRIMARY KEY AUTO_INCREMENT,
Data_Hora_Acesso DATETIME NOT NULL,
Resultado VARCHAR(50),
id_game INT,
id_escola INT,
FOREIGN KEY (id_game) REFERENCES Game(ID_Game),
FOREIGN KEY (id_escola) REFERENCES Escola(ID_Escola)
);
CREATE TABLE IP_Autorizado (
ID_Ip INT PRIMARY KEY AUTO_INCREMENT,
IP VARCHAR(45) NOT NULL,
id_escola INT,
FOREIGN KEY (id_escola) REFERENCES Escola(ID_Escola)
);
INSERT INTO Game (Nome_game, Faixa_etaria, Status_game, Tem
a_game)
VALUES
('Matematica Kids', '10+', 'Ativo', 'Educacional'),
('Historia BR', '12+', 'Ativo', 'Historia');
INSERT INTO Pacote (Nome_pacote, Preco_pacote, Limite_de_Ac
essos)
VALUES
('Basico', 99.90, 100),
('Premium', 199.90, 500);
INSERT INTO Escola (Nome_Escola, Cnpj_Escola, Status_do_Pac
ote, ID_Pacote)
2
Entrega 2 - 11/05
VALUES
('FECAP', '60.736.683/0001-71', 'Ativo', 1);
INSERT INTO Acesso (Data_Hora_Acesso, Resultado, id_game, i
d_escola)
VALUES
('2026-05-07 10:30:00', 'Sucesso', 1, 1);
INSERT INTO IP_Autorizado (IP, id_escola)
VALUES
('192.168.0.10', 1)
