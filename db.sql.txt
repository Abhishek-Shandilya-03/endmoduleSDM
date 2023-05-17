create table employee(
empid int primary key,
ename varchar(20),
edept varchar(20),
eprojects varchar(20),
constraint foreign key(eprojects) references pmanager(projects));

create table pmanager(
pid int primary key,
pname varchar(20),
pupdate varchar(20),
teams varchar(20),
constraint foreign key(teams) references projects(teams)
);

create table projects(
teams varchar(20) primary key,
name varchar(20));

create table dmanagers(
did int primary key,
dname varchar(20),
dstatus varchar(20),
teams varchar(20),
deadline date,
constraint foreign key(teams) references projects(teams));

