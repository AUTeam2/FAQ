# FAQ
Often asked questions

1. [På dansk](#Dansk)
2. [In english](#English)

# Dansk <a name="Dansk"></a>

## Generel information:
Lad være med at lave ændringer til andet end det prøvestands modul som I selv arbejder med, da dette ellers kun vil give problemer. Hvis I gør dette og der kommer problemer, er der ikke andre løsninger end at geninstaller containeren, og kopiere jeres modul over i den nye container.

Q:|*Hvordan sætter jeg det op?*
---------|---------
A:|Læs dokumentationen på [Github](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|*Virker containeren på Windows?* 
---------|---------
A:|Nej. Denne container virker ikke på Windows, kun på Linux.


Q:|*Jeg har problemer med installering af Docker* 
---------|---------
A1:|Læs informationerne på [installerings guide](https://docs.docker.com/engine/install/)
A2:|Selinux kan godt stoppe diverse ting i docker og skal derfor sættes til permissive, læs informationer på [selinux guide]((https://www.thegeekdiary.com/what-are-selinux-modes-and-how-to-set-them/))


Q:|*Vores prøvestand reagerer ikke på det modtaget signal fra webinterfacet, hvorfor?*
---------|---------
A:|Tjek om JSON protokollen er sat op korrekt på Prøvestanden.


Q:|*Vi kan ikke sende fra prøvestanden til webinterfacet…*
---------|---------
A:|Systemet beregnet til at køre på au’s interne net så prøv at VPN ind på au’s net.


Q:|*Hvordan får vi en prøvestandsside på webinterfacet?*
---------|---------
A:|Der ligger en guide på github under standarder kaldet [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|*Hvordan ændrer jeg Demo_module så den passer til vores prøvestand?*
---------|---------
A:|Der ligger en guide til hvad og hvordan I skal ændre i moduler under standarder kaldet [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:*|Hvad bruger i til at programmere i?*
---------|---------
A:|Pycharm, en pro version kan fås ved at oprette en bruger med jeres au mail, guides ligger til allle brugte teknlologier ligger på vores [github](https://github.com/AUTeam2/Guides-and-Tutorials)


Q:|*Kan i vise mig hvordan jeg bruger docker compose?*
---------|---------
A:|Der er oprettet videoguides [her](https://github.com/AUTeam2/standards/blob/master/Videoguides.md), ellers prøv google...


Q:|*Jeg har problemer med databasen i min container hvordan løser jeg det?*
---------|---------
A:|Alt dokumentation omkring databasen, og hvordan man løser fejl kan findes [her](https://github.com/AUTeam2/standards/blob/master/db-migrations.md)


Q:|*Hvordan starter jeg MQTT-brokeren?*
---------|---------
A:|Hvis man er udenfor containeren bruges denne kommando:<br>**docker-compose exec webinterface python manage.py start_messagehandler**<br>Yderligere info findes [her](https://github.com/AUTeam2/server-setup/blob/master/README.md)


Q:|*Hvordan laver man en ny admin bruger på server setuppet?* (vil til sidst kun virke på local git download af systemet)
---------|---------
A:|Hvis man er udenfor containeren bruges denne kommando:<br>**docker-compose exec webinterface python manage.py createsuperuser --username   ditnavn --email din@email.dk**<br>Yderligere info findes [her](https://github.com/AUTeam2/server-setup/blob/master/README.md)

# English <a name="English"></a>
## Generel information:
Dont make any changes, except for the test module your working with, or it could create problems in the system. If you change something your not supposed to, and it wrecks the system, the best solution would be to reinstall the server setup, and copy your module into the freshly created container. 

Q:|*How can I do the setup?*
---------|---------
A:|Read the documentation on [Github](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|*Does the container work on Windows?* 
---------|---------
A:|No. The server is made for Linux distributions.


Q:|*JI have trouble installing Docker* 
---------|---------
A1:|Read the information in [installing guide](https://docs.docker.com/engine/install/)
A2:|Selinux can create trouble for docker, and should be set in permissive mode, read how in this [selinux guide]((https://www.thegeekdiary.com/what-are-selinux-modes-and-how-to-set-them/))


Q:|*Our test setup wont respond to the signal from the webinterface, why?*
---------|---------
A:|Check and see if your JSON setup corresponds to our JSON protocols for the webinterface 


Q:|*We can't send from our test setup to the webinterface...*
---------|---------
A:|The system is supposed to run on au's internet, so try a VPN connection to au's internet.


Q:|*How do we create a test setup site in the webinterface?*
---------|---------
A:|There's a guide on github under "standarder" called [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|*Who do I change Demo_module so it fits our test setup?*
---------|---------
A:|There's a guide on github, describing how and what to do under under "standarder" called [Guide_modul_v2](https://github.com/AUTeam2/standards/blob/master/Guide_modul_v2.pdf)


Q:|*What IDE are you writing the program in?*
---------|---------
A:|Pycharm, a pro version is available by using your au mail, guides to all used technologies is on our [github](https://github.com/AUTeam2/Guides-and-Tutorials)


Q:|*Can you show me how to use docker-compose?*
---------|---------
A:|There are video guides [here](https://github.com/AUTeam2/standards/blob/master/Videoguides.md), ellers prøv google...


Q:|*I have problems with my database in my container, how do I fix it?*
---------|---------
A:|Theres documentation on the database and how to use it [here](https://github.com/AUTeam2/standards/blob/master/db-migrations.md) and [here](https://github.com/AUTeam2/standards/blob/master/anvendelse_af_databasen_i_webinterface.pdf)


Q:|*How do I start the MQTT-broker?*
---------|---------
A:|Outside of the container, this commando can be used:<br>**docker-compose exec webinterface python manage.py start_messagehandler**<br>More information can be found [here](https://github.com/AUTeam2/server-setup/blob/master/README.md)


Q:|*How do I make a new admin user on the server setup?* (in the end it will only work on a local version of the system)
---------|---------
A:|Outside of the container, this commando can be used:<br>**docker-compose exec webinterface python manage.py createsuperuser --username   ditnavn --email din@email.dk**<br>More information can be found [here](https://github.com/AUTeam2/server-setup/blob/master/README.md)
