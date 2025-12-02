## Part 1 (Individual)

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

## Part 2 (Parelles)

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

## Part 3 (Grup)

El grup ha de generar un document amb els següents punts resolts:

1\)      Dades Objecte de Còpia

Quines dades es copien i amb quina freqüència (separant Servidor/Clients i crítiques/no crítiques).

Datos del servidor de archivos Ubuntu Server

| Tipos de datos  | Volumen  | Criticidad | Frecuencia |
| :---- | :---- | :---- | :---- |
| Documentos de proyectos (Planos, especificaciones técnicas, etc) | 300 GB con un crecimiento moderado | Crítico | Diária: Incremental Semanal: Completa Mensual: Completa |
| Base de datos (Compatibilidad y clientes) | 20 GB pero con cambios constantes | Muy crítico | Cada 4 horas: Incremental Diaria: Completa Semanal: Completa Mensual: Completa |
| Carpetas personales de los usuarios (Para el trabajo diario) | 100 GB  | Crítico o médio crítico | Diária: Incremental Semanal: Completa |

### Datos de los clientes Windows 10/11

Solo se realizan las copias de:

| Tipos de datos | Criticidad | Frecuencia |
| :---- | :---- | :---- |
| Carpeta de Documentos de los usuarios | Crítico o médio crítico | Diária: Incremental Semanal: Completa |

Solo hacemos copias de eso y sólo diaria y semanal por que los clientes trabajan directamente con datos que se encuentra en el servidor y solo hace falta hacer copias de la carpeta de documentos por que algunos clientes se guardan cosas o archivos de forma temporal en la carpeta de documentos

2\)      Cronograma Setmanal Detallat

| Dia | Dades (Ex: BD) | Tipus de còpia | Mitjà |
| :---- | :---- | :---- | :---- |
| Dilluns | 1.Las bases de datos. 2.Los proyectos y las carpetas.  3.Del personal y de los clientes. | 1.Incrementales cada 4 horas a más una completa tarde de la noche tipo 23:00 h. 2.Incremental. 3.Incremental. | 1.NAS 2.NAS 3.NAS |
| Dimarts | 1.Las bases de datos. 2.Los demás datos. | 1.Incrementales cada 4 horas. 2.Incremental. | 1.NAS 2.NAS |
| Dimecres | 1.Las bases de datos. 2.Los demás datos. | 1.Incrementales cada 4 horas. 2.Incrementales. | 1.NAS 2.NAS |
| Dijous | 1.Las bases de datos. 2.Los demás datos. | 1.Incrementales cada 4 horas. 2.Incrementales. | 1.NAS 2.NAS  |
| Divendres | 1.Las bases de datos. 2.Los demás datos. | 1.Incrementales cada 4 horas. 2.Incrementales. | 1.NAS 2.NAS |
| Dissabte | 1.Las bases de datos. 2.Los demás datos. | 1.Completa semanal. 2.Completa semanal. | 1.NAS \+ Discos duros externos. 2.NAS \+ Discos duros externos. |
| Diumenge | 1.Las bases de datos. 2.Los demás datos. | Si es el primer domingo del mes tendría que ser copias completas mensuales. | Cloud cifradas ya que así serían copias externas y seguras. |

3\)      Elecció de Mitjans i Ubicació (Regla 3-2-1)

·         Mitjà 1 (Local): Quin mitjà concret (p. ex., Disc dur USB, NAS) s'utilitza.

NAS interno con un RAID 5

\-Estaría ubicado en el centro de procesamientos de datos de la empresa.

\-Estaría almacenado todas las copias incrementales como también las copias completas semanales.

\-Tendría un acceso rápido por si hace falta hacer restauraciones rápidas.

\-El RAID 5 es por si falla algún disco.

·         Mitjà 2 (Extern): Quin mitjà (p. ex., Cloud, LTO) i el proveïdor proposat (p. ex., Azure, Google Cloud, servei local).

Disco duro externo  con USB

\-Estaría comentado solo durante la realización de las copias de seguridad semanales y de las mensuales.

\-Tendría una protección por ejemplo contra las fallas eléctricas, etc.

\-Podríamos dejarlo en una caja fuerte dentro del centro de procesamientos de datos o fuera de la empresa en algún lugar seguro.

·        Ubicació Fora de Lloc: On es guarda la còpia externa (física o lògica) i qui és el responsable de la seva gestió.

Cloud y estaría subido en la nube

\-Tendría una ubicación segura en la nube.

\-Tendría una copia cifrada.

\-El responsable sería el departamento de IT de la empresa y tendrían que hacer una tipo validación mensual de la integridad.

4\)      Estratègia de Recuperació (RTO/RPO)

Com es garanteix que les dades de Comptabilitat/Clients compleixen amb el requisit de RPO (4 hores) i RTO (4 hores).

Primero que todo tenemos que dejar claro que el RPO no es lo mismo que el RTO, el RPO es como un máximo de pérdida de 4 horas y el RTO es la restauración completa en menos de 4 horas  
Para garantizar el cumplimiento de la base de datos de contabilidad y de los clientes que cumplan con el requisito RPO y RTO haremos lo siguiente:

RPO \= Máximo de 4 horas de pérdida.

Haremos copias de seguridad incrementales cada 4 horas de la base de datos y en caso de un error siempre tendrá que haber un punto de restauración menor a 4 horas.

RTO \= Restauración completa en menos de 4 horas.

Las copias tendrían que guardarse en el NAS interno y tendría que tener acceso directo y ancho de banda interno un poco elevado. A más una restauración de la base de datos de 20 GB desde el NAS. También tendría que haber un sistema de restauración automatizado.

Algunos escenarios de recuperación:

\-Falla del servidor: Tendríamos que hacer una restauración desde el NAS

\-Ransomware en el servidor: Si por algún caso no se podría usar el NAS tendríamos que hacer una restauración desde disco duro externo.

\-Desastres físicos: Tendríamos que hacer una restauración desde el Cloud mensual que tardaria mucho más o como las bases de datos tendrán una copia semanal en el disco duro externo podríamos hacer la restauración desde ahí





[Tornar a enunciat](README.md)
