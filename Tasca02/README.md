# T02: DPR — Còpies de Seguretat  
## Cas Pràctic

# Introducció al cas
A la tasca anterior heu dissenyat una política de còpies de seguretat per al client **"Muntatges i Serveis Tècnics SL"**.  
Ara toca portar a la pràctica l’estudi anterior. El client demana guies tècniques amb proves de concepte perquè el seu personal pugui implantar el pla de còpies.

---

# Part 1: Còpia de seguretat dels equips clients Windows

Encara que el DPR no contemplaria còpies dels equips clients, se’ns demana una **excepció** amb l’equip Windows del director, on es guarda informació important que no vol al servidor.

La política de còpies seguirà l’esquema **3-2-1**:  
- Una còpia al **disc secundari local**  
- Una còpia al **cloud (Google Drive)** utilitzant **Duplicati**

## Prova de concepte
- Crear una **màquina virtual Windows 11** amb dos discos:  
  - Disc principal: sistema operatiu  
  - Disc secundari: 10 GB per a les còpies
- Per Google Drive: usar un compte personal (no el del centre).

### Requisits del pla de còpies (Windows)
- Còpia del **perfil d’usuari cada hora** al disc secundari.
- **Còpia diària a les 18:00** a Google Drive.

### Tasques a documentar
1. Procediment d’instal·lació de **Duplicati**.  
2. Configuració del **pla de còpies local** i del **pla cap al cloud**.  
3. Afegir arxius a *Documents* i altres carpetes per observar el funcionament.  
4. Esborrar Documents i **restaurar** des del disc secundari.  
5. Realitzar i comprovar una **restauració des de Google Drive**.

---

# Part 2: Còpia de seguretat al servidor Linux

La solució proposada és **Duplicity**, que permet còpies locals i remotes. Combinat amb **cron**, permet crear polítiques de còpia automatitzades.

Per la guia es crearà una màquina virtual **Ubuntu Server** amb un segon disc de 10 GB (unitat auxiliar).

### Tasques a realitzar

1. Inicialitza el disc i formata’l en **xfs**.  
   - Muntar-lo manualment a `/media/backup` (creant abans la carpeta).  
2. Instal·lar **duplicity**.  
3. Crear **2 usuaris addicionals** i generar 4 arxius de 10 MB a la carpeta home de l’usuari principal.  
4. Fer una **còpia de seguretat de `/home`**.  
5. Esborrar els arxius i fer un **restore** per comprovar-ho.  
6. Afegir un arxiu de 4 MB i fer una nova còpia → ha de ser **incremental**.  
7. Desmuntar la unitat de backup.

---

## Automatització amb scripts i cron

La unitat de backup **ha d’estar desmuntada per defecte**.  
El procés sempre serà:

1. Muntar la unitat  
2. Fer la còpia  
3. Desmuntar la unitat  

### 7. Script `fullbackup.sh`
Ha de:
- Realitzar la còpia **completa** de `/home`.
- Usar la variable d’entorn `PASSPHRASE`:
  ```sh
  export PASSPHRASE=contrasenya
- Emmagatzemar la còpia al volum muntat.

- Tenir permisos d’execució.

8. Programació amb cron

Com a root, programar:

Cada diumenge a les 23:00 → execució de fullbackup.sh

9. Script incrementalbackup.sh

Ha de:

- Fer còpies incrementals de /home.

- Usar PASSPHRASE igual que l’anterior.

- Tenir permisos d’execució.

10. Programació amb cron

Com a root, programar:

De dilluns a dissabte a les 23:00 → execució de incrementalbackup.sh

Materials i Links de suport

Duplicati: https://duplicati.com/

WayToIT – Creació d’arxius amb fsutil (Windows):
https://waytoit.wordpress.com/2015/03/15/creando-archivos-con-fsutil/

WayToIT – Creació d’arxius de prova en Linux:
https://waytoit.wordpress.com/2015/03/21/creando-archivos-de-prueba-en-linux/

Duplicity man page:
http://manpages.ubuntu.com/manpages/trusty/man1/duplicity.1.html

Programar tasques amb cron:
https://geekytheory.com/programar-tareas-en-linux-usando-crontab


Si vols també te’l puc deixar en **PDF, Word, o .md descarregable**, només digues-ho!


[Solucio](solucio.md)

[Tornar pàgina projecte](../README.md)
