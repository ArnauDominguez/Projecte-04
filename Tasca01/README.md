## T01: DRP: còpies de seguretat. Estudi cas client (treball cooperatiu)
# Introducció
La primera hora el vostre responsable de seguretat us presenta el tema de les còpies de seguretat a partir d’un material didàctic. A continuació, caldrà que hi treballeu els aspectes del tema i ho fareu mitjançant una dinàmica cooperativa.

# Presentació del cas client
**"Muntatges i Serveis Tècnics SL"** és una petita empresa dedicada a la instal·lació i manteniment d'equips industrials.

## Infraestructura Tècnica
- **Servidor de Fitxers (Ubuntu Server):**
  - *Documents de Projectes:* Plànols, especificacions tècniques (300 GB, creixement moderat).
  - *Bases de Dades (Comptabilitat i Clients):* Crítiques i d'ús diari (20 GB, canvi constant).
  - *Carpetes Personals dels Usuaris:* Per a la feina diària (100 GB).
- **10 Equips Clients (Windows 10/11):** Alguns tècnics guarden temporalment informes i arxius crítics a "Documents".
- **Connexió a Internet:** Fibra 600 Mbps simètrica.

## Requisits de Recuperació
- **RTO:** Menys de 4 hores per a Comptabilitat/Clients.
- **RPO:** 
  - Pèrdua màxima de 24 h per a la majoria de dades.
  - Comptabilitat/Clients: màxim 4 h.
- **Retenció:** Historial mínim d’un mes.

# Fase 1: Treball individual
1. **Què copiar?** Dades crítiques i si cal copiar els clients.
2. **Periodicitat i Tipus:** Diari/Setmanal/Mensual + Completa/Diferencial/Incremental.
3. **Mitjans i Ubicació:** Discs, NAS, Cloud, Cintes. Aplicar regla 3-2-1.

# Fase 2: Treball per parelles
1. **Comparació i consens** de les respostes.
2. **Creació d’un esquema 3-2-1** unificat.

### Taula
| Element                  | Proposta de la Parella | Justificació |
|-------------------------|-------------------------|--------------|
| **Dades Crítiques**     |                         |              |
| **Periodicitat (BD)**   |                         |              |
| **Tipus de Còpia (BD)** |                         |              |
| **Mitjà 1 (Local)**     |                         |              |
| **Mitjà 2 (Extern)**    |                         |              |

# Fase 3: Treball en grup
1. **Debat i selecció.**
2. **Redacció de la Política de Còpies** final.

# Document Final
## 1) Dades Objecte de Còpia
Freqüència i classificació Servidor/Clients + Crítiques/No crítiques.

## 2) Cronograma Setmanal

| Dia     | Dades | Tipus | Mitjà |
|---------|--------|--------|--------|
| Dilluns |        |        |        |
| Dimarts |        |        |        |
| ...     |        |        |        |
| Diumenge|        |        |        |

## 3) Mitjans i Ubicació (3-2-1)
- **Mitjà 1 (Local):** USB, NAS, etc.
- **Mitjà 2 (Extern):** Cloud / Cintes.
- **Off-site:** Ubicació i responsable.

## 4) Estratègia de Recuperació
Garantint RTO/RPO de 4 h per Comptabilitat/Clients.

# Materials i Links
- Moodle 0226 Seguretat Informàtica RA2.AA3 Còpies  
- INCIBE – Guía de copias de seguridad  
- Xataka – Backup 3-2-1 (YouTube): https://youtu.be/PM_M4Iz6I4o?si=F7DRyDDTZE3hjWn8

 [Solucio](solucio.md)

[Tornar pàgina projecte](../README.md)
