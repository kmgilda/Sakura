Sakura - Natural Language Search Engine

MySQL Database commands:

create database sakura; 
use sakura;

MySQL Create table commands :

create table SearchEngine (id INT NOT NULL AUTO_INCREMENT,websitelink VARCHAR(255) NOT NULL, websitetext TEXT, PRIMARY KEY (id), FULLTEXT KEY (websitetext));   
alter table SearchEngine add UNIQUE (websitelink);

create table UserSearches (id INT NOT NULL auto_increment, searchterm TEXT, PRIMARY KEY (id), FULLTEXT KEY (searchterm));

Dummy data : 

INSERT INTO SearchEngine (websitelink,websitetext) values ("https://www.google.co.in/","Search the world's information, including webpages, images, videos and more"); 
INSERT INTO SearchEngine (websitelink,websitetext) values ("http://www.bing.com/","Bing helps you turn information into action, making it faster and easier to go from searching to doing.");

insert into UserSearches (searchterm) values ("search"); 
insert into UserSearches (searchterm) values ("information"); 
insert into UserSearches (searchterm) values ("bing");
