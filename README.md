# 📈 Énergie renouvelable : Prédiction de la date de la prochaine production d’électricité de 1000 kWh par des panneaux solaires et à partir des prévisions météorologiques


## Contexte

Après avoir constaté qu'il n'existait pas d'ensemble de données rassemblant à la fois les conditions météorologiques et l'énergie solaire, permettant d'analyser et de prédire la production solaire en fonction des conditions météorologiques, j'ai décidé de récupérer cet ensemble de données.



## Ensemble de données

J'ai trouvé un bon jeu de données sur kaggle «  Daily Power Production of Solar Panels » décrivant la production de panneaux solaires. 
Ils ont pu collecté ces données à partir d’octobre 2011 car ils ont  installé des panneaux solaires (ou modules photovoltaïques) sur leur toit. La puissance totale des modules est de 5kWp.

Le fichier « solarpower_cumuldaybyday2 » comporte deux colonnes : d'abord la date et ensuite la puissance cumulée en kWh.
Ce fichier permet donc de visualiser la puissance solaire cumulée jour par jour depuis 2011.

Par ailleurs, j’ai récupéré un fichier enregistrant au quotidien une consommation d'électricité, puis la production d'électricité des panneaux solaires. 

Le fichier « PV_Elec_Gas2 » correspond donc à  une production quotidienne cumulée d'énergie solaire par les panneaux photovoltaïques. Il y a aussi des colonnes avec la consommation journalière d'électricité et de gaz. Les mesures sont prises le matin entre 7h et 8h, elles sont donc corrélées à la météo de la veille.

Ce fichier « PV_Elec_Gas2 » est séparé par des ';' et comporte 4 colonnes : Date, Puissance solaire cumulée, kWh d'électricité utilisés, m² de gaz utilisés.


Il reste à obtenir les données météorologiques de la région où se trouvent ces panneaux (Anvers en Belgique). J'ai donc récupéré ces données sur le site Time And Date (les fichiers « weather_in_Antwerp_future2 » & « weather_in_Antwerp »).
Cet ensemble de données contient les conditions météorologiques (vent, humidité, pression atmosphérique et température) à Anvers en Belgique, de 2012 à 2019.
Il s'agit de la même période pour le jeu de données Daily Power Production of Solar Panels.





## Problématique

Cet ensemble de données me parraissait intéressant à rassembler et à exploiter pour traiter différentes problématiques liées à l’énergie renouvelable, du type :

- Quels sont les facteurs météorologiques qui affectent le plus la quantité d'énergie renouvelable produite par les panneaux solaires ?
- Devrions-nous éteindre complètement les panneaux solaires certains mois de l’année, au cas où ils ne produiraient pas d'énergie ?
- La pression atmosphérique influence-t-elle la production d'énergie même si la journée est ensoleillée ?

NB : Il est intéressant de noter que l'orientation des panneaux solaires est OSO, ce qui signifie que la plus grande partie de l'énergie est produite l'après-midi, avec un pic entre 15h00 et 19h00 en été.

Dans ce use case, nous allons prédire la date de la prochaine production de 1000kWh par des panneaux solaires et à partir des prévisions météorologiques.




## Démarche suivie pour résoudre le problème

Cf. le notebook ci-joint.

Ce guide permet de prédire la date de la prochaine production de 1000kWh par des panneaux solaires et à partir des prévisions météorologiques.



