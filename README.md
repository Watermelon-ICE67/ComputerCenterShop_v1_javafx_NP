# ComputerCenterShop — pràctica integradora RA2

> **Plantilla de l'equip.** Copieu aquest fitxer al vostre repositori de treball i completeu-lo a mesura que avanceu. No inclou solucions de codi: les decisions, proves i explicacions han de ser vostres.

## Fitxa de l'equip

- Integrants: **[Noel Alvarez]** i **[Pau Nuet]**
- Repositori compartit: **[https://github.com/Watermelon-ICE67/ComputerCenterShop_v1_javafx_NP.git]**
- Branca de treball habitual: **[Main]**
- Data d'inici: **[17/11/2026]**
- Última actualització: **[AAAA-MM-DD]**

## Propòsit del projecte

En aquesta pràctica desenvolupem una aplicació Java que accedeix a una base de dades relacional amb JDBC. Treballem sobre el projecte *starter* indicat pel professorat i fem servir el backlog RA2 per organitzar les tasques, els commits, les proves i les decisions tècniques.

El repositori ha de mostrar el procés de treball real de l'equip. No es tracta només d'arribar a una aplicació que s'executi: també cal poder explicar què s'ha canviat, com s'ha comprovat i per què la decisió correspon a cada *issue*.

## Punt de partida

- Repositori *starter* utilitzat: **[https://github.com/Watermelon-ICE67/ComputerCenterShop_v1_javafx_NP.git]**
- Gestor de base de dades relacional utilitzat: **[HP]**
- Connector utilitzat: **[Jdbc]**
- Entorn de desenvolupament: **[Eclipse]**
- Comandament o acció que fem servir per comprovar l'execució: **[clean javafx:run]**

> No incorporeu ORM, Hibernate, ObjectDB, MongoDB, serveis externs ni persistència principal en fitxers. Aquests elements no formen part de RA2.

## Com treballem cada *issue*

1. Llegim l'objectiu i els criteris d'acceptació de l'*issue*.
2. Acordem què ha de canviar i qui inicia la feina.
3. Fem canvis petits i comprensibles, amb *commits* que expliquin la decisió.
4. Provem el comportament esperat i en guardem una evidència.
5. Actualitzem aquest README amb el resultat, la prova i l'enllaç al *commit* o a la *pull request*.
6. Tanquem l'*issue* només quan l'equip pot explicar individualment la solució aplicada.

## Progrés del backlog

Marqueu una tasca quan la prova i el rastre al repositori estiguin recollits. Els enllaços apunten a l'enunciat, no a una solució.

### M1 · Base JDBC operativa

- [X] [RA2-ISSUE-01 · Preparar el projecte JDBC](issues/RA2-ISSUE-01-preparar-projecte-jdbc.md)
- [X] [RA2-ISSUE-02 · Connector, URL i connexió](issues/RA2-ISSUE-02-revisar-connector-url-connexio.md)
- [X] [RA2-ISSUE-03 · Estructura relacional](issues/RA2-ISSUE-03-crear-estructura-relacional.md)

### M2 · Operacions relacionals principals

- [X] [RA2-ISSUE-04 · Inserció de dades](issues/RA2-ISSUE-04-inserir-producte-preparedstatement.md)
- [ ] [RA2-ISSUE-05 · Actualització d'estoc](issues/RA2-ISSUE-05-actualitzar-estoc.md)
- [ ] [RA2-ISSUE-06 · Eliminació controlada](issues/RA2-ISSUE-06-eliminar-producte-controlat.md)
- [ ] [RA2-ISSUE-07 · Consultes i resultats](issues/RA2-ISSUE-07-consultar-inventari-resultset.md)

### M3 · Robustesa JDBC

- [ ] [RA2-ISSUE-08 · Tancament de recursos](issues/RA2-ISSUE-08-tancar-recursos.md)
- [ ] [RA2-ISSUE-09 · Transaccions](issues/RA2-ISSUE-09-transaccio-commit-rollback.md)
- [ ] [RA2-ISSUE-10 · Procediment amb paràmetres](issues/RA2-ISSUE-10-procediment-parametres.md)
- [ ] [RA2-ISSUE-11 · Errors de connexió i operacions](issues/RA2-ISSUE-11-errors-connexio-recursos.md)

### M4 · Documentació i tancament

- [ ] [RA2-ISSUE-12 · Documentar l'execució i la configuració](issues/RA2-ISSUE-12-documentar-execucio-configuracio.md)
- [ ] [RA2-ISSUE-13 · Preparar el lliurament de la pràctica](issues/RA2-ISSUE-13-lliurament-practica-integradora.md)

## Registre de treball

Dupliqueu aquest bloc per a cada *issue* que completeu. Escriviu amb les vostres paraules i enllaceu només proves i *commits* del vostre repositori.

### RA2-ISSUE-XX · [títol de l'*issue*]

- Estat: **pendent | en curs | comprovat**
- Persona que l'ha iniciat: **[nom]**
- Problema inicial: **[què no funcionava o què faltava]**
- Decisió aplicada: **[què heu decidit fer i per què]**
- Canvis fets: **[fitxers o parts del projecte modificades]**
- Prova realitzada: **[cas que heu provat i resultat observat]**
- Evidència: **[]**
- *Commit* o *pull request*: **[enllaç o identificador]**
- Explicació individual: **[què pot explicar cada integrant sobre aquesta tasca]**
- Ús d'IA, si n'hi ha hagut: **[consulta feta, ajuda rebuda i comprovació pròpia]**


### RA2-ISSUE-01 · [Preparar el projecte JDBC]

- Estat: **comprovat**
- Persona que l'ha iniciat: **[Pau]**
- Problema inicial: **[Verificar el funcionament]**
- Decisió aplicada: **[Instal·lar, compilar i executar]**
- Canvis fets: **[Executar desde el build]**
- Prova realitzada: **[Executar desde el build]**
- Evidència: **[veure captura1]**
- *Commit* o *pull request*: **[fe82412]**
- Explicació individual: **[què pot explicar cada integrant sobre aquesta tasca]**
- Ús d'IA, si n'hi ha hagut: **[consulta feta, ajuda rebuda i comprovació pròpia]**

### RA2-ISSUE-02 · Connector, URL i connexió

- Estat: **comprovat**
- Persona que l'ha iniciat: **Pau Nuet**
- Problema inicial: **`connect()` només llegia les propietats de sistema i llançava l'excepció "RA2-ISSUE-02 pendent" sense obrir cap connexió.**
- Decisió aplicada: **Obrir la connexió amb `DriverManager.getConnection(url, user, password)` i guardar-la al camp `conn`. Es mantenen les propietats `computercenter.db.url`, `computercenter.db.user` i `computercenter.db.password`, amb valors per defecte d'H2 local, perquè la configuració es pugui canviar sense tocar el codi.**
- Canvis fets: **`src/dao/ProductDaoImplJDBC.java` (mètode `connect()`).**
- Prova realitzada: **Execució de `Ra2JdbcDemo`. Ja no apareix l'error de RA2-ISSUE-02 i el programa s'atura a l'error de RA2-ISSUE-03 (`initSchema`), que encara és pendent.**
- Evidència: **[veure captura2]**
- *Commit o pull request*: **[fe82412]**
- Explicació individual: **Puc explicar que `DriverManager` obre la connexió JDBC a partir de la URL, l'usuari i la contrasenya; que el connector és la dependència d'H2 del `pom.xml`; que `System.getProperty(clau, valorPerDefecte)` permet canviar la configuració amb `-D`; i que la connexió es guarda a `conn` perquè la resta de mètodes del DAO la puguin reutilitzar.**

### RA2-ISSUE-03 · Implementar estructura relacional

- Estat: **comprovat**
- Persona que l'ha iniciat: **Pau Nuet**
- Problema inicial: **`initSchema()` només llançava l'excepció "RA2-ISSUE-03 pendent" i no creava cap taula.**
- Decisió aplicada: **Crear amb DDL, des del DAO i amb `Statement` dins d'un try-with-resources, les taules `products` i `inventory_history` (amb clau forana a `products`) i l'alias `STOCK_ALERT_LIMIT` que apunta al mètode `stockAlertLimit`. Es fa servir `CREATE ... IF NOT EXISTS` i el seed de 3 productes només s'insereix si la taula `products` és buida, perquè no es dupliquin dades en executar-ho més d'una vegada.**
- Canvis fets: **`src/dao/ProductDaoImplJDBC.java` (mètode `initSchema()` i import de `Statement`).**
- Prova realitzada: **Execució de `Ra2JdbcDemo` dues vegades: `initSchema()` passa sense error i el programa s'atura a l'error de RA2-ISSUE-07 (`getInventory`), que encara és pendent. La segona execució dona el mateix resultat, sense duplicats.**
- Evidència: **[veure captura 3]**
- *Commit o pull request*: **[fe82412]**
- Explicació individual: **Puc explicar què és un DDL i per què faig servir `IF NOT EXISTS`; què fa la clau forana entre `inventory_history` i `products`; què és un alias a H2 i com enllaça amb el mètode Java `stockAlertLimit`; i per què comprovo `COUNT(*)` abans d'inserir el seed perquè no es dupliquin productes.**

### RA2-ISSUE-04 · Implementar inserció amb PreparedStatement

- Estat: **comprovat**
- Persona que l'ha iniciat: **Pau Nuet**
- Problema inicial: **`insertProduct()` només llançava l'excepció "RA2-ISSUE-04 pendent" i no inseria cap producte a la base de dades.**
- Decisió aplicada: **Fer la inserció amb `PreparedStatement` i la sentència `INSERT INTO products(name, wholesaler_price, available, stock) VALUES (?, ?, ?, ?)`, assignant cada valor amb els setters i retornant el resultat d'`executeUpdate()` (files afectades). No es concatenen valors dins del SQL, i l'`id` el genera la base de dades.**
- Canvis fets: **`src/dao/ProductDaoImplJDBC.java` (mètode `insertProduct()` i import de `PreparedStatement`).**
- Prova realitzada: **Com que la consulta de l'ISSUE-07 encara és pendent, he fet una classe de prova temporal que insereix `Dock USB-C` i després consulta la taula amb JDBC. La inserció retorna 1 fila afectada i el producte apareix a la consulta posterior amb preu 35.00 i estoc 4.**
- Evidència: **[veure captura4]**
- *Commit o pull request*: **[fe82412]**
- Explicació individual: **Puc explicar què és un `PreparedStatement` i per què els `?` eviten concatenar valors i la injecció SQL; què retorna `executeUpdate()`; per què l'`id` no s'assigna a mà (columna `IDENTITY`); i per què vaig haver de fer una prova a part per veure la consulta posterior.**

## Proves que hem de poder repetir

| Cas que comprovem | Dades o condicions inicials | Resultat observat | Evidència |
| --- | --- | --- | --- |
| Arrencada del projecte | **[completeu]** | **[completeu]** | **[enllaç]** |
| Operació de modificació | **[completeu]** | **[completeu]** | **[enllaç]** |
| Consulta de dades | **[completeu]** | **[completeu]** | **[enllaç]** |
| Cas d'error controlat | **[completeu]** | **[completeu]** | **[enllaç]** |
| Operació agrupada o transacció | **[completeu]** | **[completeu]** | **[enllaç]** |

## Decisions i dubtes de l'equip

| Data | *Issue* | Decisió o dubte | Com s'ha resolt | Referència |
| --- | --- | --- | --- | --- |
| **[AAAA-MM-DD]** | **[RA2-ISSUE-XX]** | **[completeu]** | **[completeu]** | **[enllaç]** |

## Ús responsable d'IA

El nivell previst és **IA-1**: podeu usar eines d'IA com a suport per entendre conceptes, formular hipòtesis o revisar una explicació. No substitueixen les proves del projecte ni l'explicació individual.

Si n'heu fet ús, anoteu a l'*issue* corresponent què heu preguntat, què heu contrastat amb el projecte i quina decisió final heu pres. No enganxeu una resposta d'IA com si fos una prova de funcionament.

## Abans de donar la pràctica per preparada

- [ ] Els *issues* P0 tenen un resultat comprovat o una incidència explicada.
- [ ] El repositori conté *commits* que permeten seguir el treball de l'equip.
- [ ] Les proves de funcionament tenen evidències enllaçades.
- [ ] Les decisions sobre connector, consultes, recursos, transaccions i procediments estan explicades amb paraules pròpies.
- [ ] Tots dos integrants poden defensar individualment les decisions tècniques del repositori.
- [ ] El README no inclou solucions copiades ni contingut fora de l'abast de RA2.

---

*Aquesta plantilla és un suport per documentar el treball. El que acredita el procés és el repositori de l'equip, amb els seus canvis, proves, decisions i explicacions.*
