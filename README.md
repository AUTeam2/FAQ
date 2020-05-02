# FAQ
Often asked questions

1. [På dansk](#Dansk)
2. [In english](#English)

# Dansk <a name="Dansk"></a>

## Generel information:
Lad være med at lave ændringer til andet end det prøvestands modul som I selv arbejder med, da dette ellers kun vil give problemer. Hvis I gør dette og der kommer problemer, er der ikke andre løsninger end at geninstaller containeren, og kopiere jeres modul over i den nye container.

Q:|A:
---------|---------
Hvordan sætter jeg det op?|Læs dokumentationen på [Github](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|A:
---------|---------
Virker containeren på Windows?|Nej. Denne container virker ikke på Windows, kun på Linux.


Q:|A:
---------|---------
Jeg har problemer med installering af Docker|Læs informationerne på [installerings guide](https://docs.docker.com/engine/install/)
 ---|Selinux kan godt stoppe diverse ting i docker og skal derfor sættes til permissive, læs informationer på [selinux guide](https://www.thegeekdiary.com/what-are-selinux-modes-and-how-to-set-them/)


Q:|A:
---------|---------
Vores prøvestand reagerer ikke på det modtaget signal fra webinterfacet, hvorfor?|Tjek om JSON protokollen er sat op korrekt på Prøvestanden.


Q:|A:
---------|---------
Vi kan ikke sende fra prøvestanden til webinterfacet…|Systemet beregnet til at køre på au’s interne net så prøv at VPN ind på au’s net.


Q:|A:
---------|---------
Hvordan får vi en prøvestandsside på webinterfacet?|Der ligger en guide på github under standarder kaldet [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|A:
---------|---------
Hvordan ændrer jeg Demo_module så den passer til vores prøvestand?|Der ligger en guide til hvad og hvordan I skal ændre i moduler under standarder kaldet [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|A:
---------|---------
Hvad bruger i til at programmere i?|Pycharm, en pro version kan fås ved at oprette en bruger med jeres au mail, guides ligger til allle brugte teknlologier ligger på vores [github](https://github.com/AUTeam2/Guides-and-Tutorials)


Q:|A:
---------|---------
Kan i vise mig hvordan jeg bruger docker compose?|Der er oprettet videoguides [her](https://github.com/AUTeam2/standards/blob/master/Videoguides.md), ellers prøv google...


Q:|A:
---------|---------
Jeg har problemer med databasen i min container hvordan løser jeg det?|Alt dokumentation omkring databasen, og hvordan man løser fejl kan findes [her](https://github.com/AUTeam2/standards/blob/master/db-migrations.md)


Q:|A:
---------|---------
Hvordan starter jeg MQTT-brokeren?|Hvis man er udenfor containeren bruges denne kommando:<br>**docker-compose exec webinterface python manage.py start_messagehandler**<br>Yderligere info findes [her](https://github.com/AUTeam2/server-setup/blob/master/README.md)


Q:|A:
---------|---------
Hvordan laver man en ny admin bruger på server setuppet? (vil til sidst kun virke på local git download af systemet)|Hvis man er udenfor containeren bruges denne kommando:<br>**docker-compose exec webinterface python manage.py createsuperuser --username   ditnavn --email din@email.dk**<br>Yderligere info findes [her](https://github.com/AUTeam2/server-setup/blob/master/README.md)

# English <a name="English"></a>
## Generel information:
Dont make any changes, except for the test module your working with, or it could create problems in the system. If you change something your not supposed to, and it wrecks the system, the best solution would be to reinstall the server setup, and copy your module into the freshly created container. 

Q:|A:
---------|---------
How can I do the setup?|Read the documentation on [Github](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|A:
---------|---------
Does the container work on Windows?|No. The server is made for Linux distributions.


Q:|A:
---------|---------
JI have trouble installing Docker|Read the information in [installing guide](https://docs.docker.com/engine/install/)
---|Selinux can create trouble for docker, and should be set in permissive mode, read how in this [selinux guide]((https://www.thegeekdiary.com/what-are-selinux-modes-and-how-to-set-them/))


Q:|A:
---------|---------
Our test setup wont respond to the signal from the webinterface, why?|Check and see if your JSON setup corresponds to our JSON protocols for the webinterface 


Q:|A:
---------|---------
We can't send from our test setup to the webinterface...|The system is supposed to run on au's internet, so try a VPN connection to au's internet.


Q:|A:
---------|---------
How do we create a test setup site in the webinterface?|There's a guide on github under "standarder" called [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|A:
---------|---------
How do I change Demo_module so it fits our test setup?|There's a guide on github, describing how and what to do under under "standarder" called [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|A:
---------|---------
What IDE are you writing the program in?|Pycharm, a pro version is available by using your au mail, guides to all used technologies is on our [github](https://github.com/AUTeam2/Guides-and-Tutorials)


Q:|A:
---------|---------
Can you show me how to use docker-compose?|There are video guides [here](https://github.com/AUTeam2/standards/blob/master/Videoguides.md), ellers prøv google...


Q:|A:
---------|---------
I have problems with my database in my container, how do I fix it?|Theres documentation on the database and how to use it [here](https://github.com/AUTeam2/standards/blob/master/db-migrations.md) and [here](https://github.com/AUTeam2/standards/blob/master/anvendelse_af_databasen_i_webinterface.pdf)


Q:|A:
---------|---------
How do I start the MQTT-broker?|Outside of the container, this commando can be used:<br>**docker-compose exec webinterface python manage.py start_messagehandler**<br>More information can be found [here](https://github.com/AUTeam2/server-setup/blob/master/README.md)


Q:|A:
---------|---------
How do I make a new admin user on the server setup? (in the end it will only work on a local version of the system)|Outside of the container, this commando can be used:<br>**docker-compose exec webinterface python manage.py createsuperuser --username   ditnavn --email din@email.dk**<br>More information can be found [here](https://github.com/AUTeam2/server-setup/blob/master/README.md)
