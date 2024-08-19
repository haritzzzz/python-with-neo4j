All about the description of the file in this repo

This project can happen under the idea "I want to bring the specific details of all present champions in League of Legends like name, best rune set, best item build combined with details of all active competitive 
players like what role they play, what is the best of 3 champions they have used, what region are they play for. As a result, to find the relationship between all of these champions and players
and visualize it via some tool". With the restricted time, I can only scrap all the data and create a relationship within the neo4j database and visualize it via the "neo4j browser". but I think we can use this data
set I created to build a website that can suggest how we should play all the champions in League of Legends.

champ.ipynb is a file that I use to create a method to scrap data from 1 particular website. the idea behind this file is I have to get the specific data from 1 Champion like name, best rune set, and best spell to use. 
I use the BeautifulSoup library to scrap all the data from a website, select only data I am interested in through html tag, and put all that data into the list that I can use further. So this file is the first step that I have tried.

champions.ipynb is a file in which I use the method from champ.ipynb file to create a loop where I can get the data from all champions listed by name alphabet. In this file, I use the neo4j library to bring all the data 
that I selected into a group of data that have an attribute like their name and other details. In a graph database like neo4j, this group of data is called a node. so now I have all nodes that contain data of champions, 
spells, runes, and nodes that have the attribute of the recommended rune set and spell for each champion.

item-champions.ipynb is a file in which I use the same idea of champions.ipynb to scrap only the best item build for each champion. in the result, I have all nodes that contain data of items and nodes that have attributes of 
recommended item build for each champion.

players.ipynb is a file that I created as a method to scrap the names of all active competitive players in each region from the e-sports news website. I use this name list to select only active competitive players' information 
in another website that contains all competitive players (including all inactive players and all players that haven't played in major league) like name, role, Most played champion, team, country, and region. As a result, 
I have all nodes that contain all players, teams, regions, and roles.

after running all these files (champions.ipynb, item-champions.ipynb, players.ipynb). you will have all the nodes that can visualize via neo4j browser using cypher language to query. and I will run all the code in 
neo4j_rel_exec_comm.txt in the neo4j browser to create a relationship between each node.
