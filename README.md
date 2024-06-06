# ModBusSploit
Outils pour exploiter protocole industriel ModBus TCP

## Description
ModBusSploit est un framework complet, écrit en python3, qui peut être utilisé pour réaliser les phases d'énumération et d'exploitation pendant un test de pénétration contre le protocole Modbus TCP.


## Modules
ModBusSploit est publié avec 11 modules qui sont prêts à l'emploi !
Dans le répertoire « modules », ils sont situés dans des dossiers séparés, chacun pour un type d'analyse et/ou d'attaque spécifique.

EXPLOIT - INJECTION
* readCoil.py : lit les valeurs d'un registre de bobine cible.
* readDiscreteInput.py : lit les valeurs d'un registre discret cible.
* readHoldingRegister.py : lit les valeurs d'un registre de maintien cible.  
* readInputRegister.py : lit les valeurs d'un registre d'entrée cible.
* writeSingleCoil.py : écrit des valeurs dans un registre de bobine cible.
* writeSingleRegister.py : écrit des valeurs dans un registre cible.

EXPLOIT - DOS
* dosWriteCoils.py : exécute des attaques DOS par le biais de la fonction de bobine d'écriture.
* dosWriteRegisters.py : effectue des attaques DOS par le biais de la fonction d'écriture du registre.

AUXILIARY - SCANNER
* scanner.py : effectue un triple test pour vérifier si le Modbus fonctionne sur la cible.
* id_fuzzer.py : effectue une attaque par fuzzing pour découvrir l'ID de l'esclave.

AUXILIARY - SNIFF
* arp_poisoning.py : mettre en place une attaque de type Man-In-The-Middle entre l'esclave et le maître. Wireshark est nécessaire pour renifler les paquets.

## Installation
Vous n'avez pas besoin d'installation ! Je déteste devoir installer quelque chose écrit en python3.
Vous pouvez directement télécharger ModBusSploit et l'exécuter en utilisant :
```
./start.py
```
### Requirments
Vous devez installer quelques bibliothèques :
```
termcolor
importlib
secrets
ipaddress
scapy
```
You can easily speed up the process using:
```
pip3 install -r requirements.txt
```

## Usage
You can run it using:
```
./start.py
```
You can print the "helper" typing "help" inside ModBusSploit's console:
```
console()> help
====COMMANDS=====================================

help	Help menu
clear	Clear screen
exit	Exit the console
show	Displays all modules or options of a selected module
use	Load a specified module
back	Unload the current module
info	Displays information about a specified module or the loaded one
set	Sets a context-specific variable to a value
exploit	Run the loaded module
```
