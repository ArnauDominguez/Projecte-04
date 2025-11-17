# T03: Pla de Recuperació davant Desastres  
## Imatges del Sistema

# Introducció al cas
Recordeu el cas del portàtil al qual no es podia accedir? En aquella situació, la recuperació de l’accés i la posterior fortificació van impressionar el client, que ara ha requerit la vostra participació en un nou encàrrec.

S’ha d’elaborar un **Pla de Contingència i Continuïtat del Negoci**, i dins d’aquest, el **Pla de Recuperació davant Desastres (DRP – Disaster Recovery Plan)**.

Aquest pla contempla els processos de restauració de dades, hardware i software crític per recuperar l’activitat tan aviat com sigui possible.

Un dels punts del pla és garantir que els treballadors puguin disposar ràpidament dels seus equips en cas de robatori, avaria, etc. Per això cal **crear imatges de restauració del sistema**. El temps d’instal·lació manual (SO + configuracions + aplicacions) és inviable.

Els equips del client utilitzen **GNU/Linux Zorin OS 18**, amb diverses aplicacions ja configurades.

---

# Fase 1: Anàlisi i justificació de la solució tècnica

Cal investigar eines capaces de:
- Crear una imatge complerta del disc.
- Restaurar-la posteriorment mantenint configuracions i aplicacions.

Existeixen productes comercials i de la comunitat.

### Tasca:
- Triar **2 solucions comercials** i **2 de comunitat**.
- Fer **una comparativa real**, no text copiat.
- Incloure:
  - Característiques destacades  
  - Cost o llicència  
- Indicar **quina solució proposeu** i justificar-la basant-vos en la comparativa.

---

# Fase 2: Guia d’Ús Tècnica (Manual Operatiu)

Amb la màquina proporcionada pel client (simulada amb una OVA), realitzareu:

### Procediments:
1. **Crear una imatge completa del sistema.**
2. **Restaurar la imatge** sobre una màquina virtual neta:
   - Mateixa RAM  
   - Mateix processador  
   - Mateixa configuració de xarxa  
   - Mateixa mida de disc  
   - Cap sistema operatiu instal·lat

Heu d’elaborar una **guia tècnica detallada**, amb:
- Explicacions clares  
- Captures de pantalla significatives  
- Procediment ordenat i reproduïble  

Com és una prova de concepte i encara no hi ha producte aprovat, s’utilitzarà **Rescuezilla** per elaborar la guia.

> *Es tracta d’una tasca individual.*

---

# Materials i Links de Suport
- **INCIBE – “¿Ya tienes tu Plan de Recuperación ante Desastres?” (2019)**  
  https://www.incibe.es/empresas/blog/tienes-tu-plan-recuperacion-desastres

- **Rescuezilla – Pàgina oficial**

[Solucio](solucio.md)

[Tornar pàgina projecte](../README.md)

