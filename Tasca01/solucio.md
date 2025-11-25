## Part 1

## Què copiar? 

Dades més crítiques:

* Bases de Dades de Comptabilitat i Clients.

* Documents de Projectes.

* Carpetes Personals per treball diari.

Cal copiar els equips clients?  
 No cal còpia completa. Només la carpeta Documents dels tècnics, perquè hi guarden fitxers importants temporalment.

## Periodicitat i Tipus de Còpia

* Bases de Dades: Completa setmanal \+ Incremental cada 4 hores.

* Documents de Projectes: Completa setmanal \+ Incremental diària.

* Carpetes Personals: Completa setmanal \+ Incremental diària.

* Equips clients (Documents): Completa setmanal \+ Incremental diària.

## Mitjans i Ubicació 

Mitjans recomanats:

* NAS local (còpies diàries i ràpides).  
* Cloud (còpia externa).  
* Opcional: Disc extern per còpia setmanal.

Ubicació:

* Còpia recent: NAS local.  
* Còpia off-site:  Cloud o disc extern fora de l’empresa.

## Part 2 

| Element | Proposta de la Parella | Justificació |
| :---- | :---- | :---- |
| **Dades Crítiques** | Bases de Dades de Comptabilitat i Clients | Són les que tenen requisits més estrictes: RTO \< 4 h i RPO \< 4 h. Canvien constantment i cal prioritzar-les. |
| **Periodicitat (BD)** | Còpies incrementals cada 4 hores \+ còpia completa diària | Garanteix complir l’RPO de 4 hores. La còpia completa diària dona un punt de restauració sòlid. |
| **Tipus de Còpia (BD)** | Sistema híbrid: Completes  \+ Incrementals  | Minimitza el temps i espai, mantenint la capacitat de restauració ràpida. |
| **Mitjà 1 (Local)** | NAS intern al CPD amb RAID 5 | Còpia ràpida i restauració immediata. El RAID aporta tolerància a fallades i el NAS permet automatitzar. |
| **Mitjà 2 (Extern)** | Còpia en núvol  | Garanteix el “1 off-site” de l’esquema 3-2-1. Protegeix contra robatori, incendi o desastre físic. |

## **Explicació breu del sistema 3-2-1 implementat**

* **3 còpies:**  
  * Dades originals al servidor Ubuntu  
  * Còpia local al NAS  
  * Còpia externa al núvol  
* **2 tipus de mitjà:**  
  * Emmagatzematge local (NAS RAID)  
  * Emmagatzematge al núvol  
* **1 còpia fora de la ubicació física:**  
  * La còpia al núvol xifrada


[Tornar a enunciat](README.md)
