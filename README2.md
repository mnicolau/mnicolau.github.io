<!-- MarkdownTOC -->

- [Introducció](#introducció)
- [Dispositius basics utilitzats amb el sistema SportIdent](#dispositius-basics-utilitzats-amb-el-sistema-sportident)
    - [Bases](#bases)
    - [Xip (tarja electrònica)](#xip-tarja-electrònica)
    - [Altres dispositius](#altres-dispositius)
- [Programar les bases electròniques](#programar-les-bases-electròniques)
    - [Modes de treball](#modes-de-treball)
    - [Base SI-Master](#base-si-master)
    - [A tenir en compte...](#a-tenir-en-compte)
    - [COMPTE AMB LA BASE USB!!](#compte-amb-la-base-usb)
    - [Programari utilitzat](#programari-utilitzat)
    - [SI-Boot](#si-boot)
- [Programa de gestió de curses: OE2010 (v.11)](#programa-de-gestió-de-curses-oe2010-v11)
    - [Versions](#versions)
    - [Introduir la llicència](#introduir-la-llicència)
    - [Gestió de curses de varis dies](#gestió-de-curses-de-varis-dies)
    - [Crear una CURSA (esdeveniment)](#crear-una-cursa-esdeveniment)
    - [CONFIGURACIÓ DE L'ESEDEVENIMENT](#configuració-de-lesedeveniment)
    - [COPIA DE SEGURETAT](#copia-de-seguretat)
    - [INSCRIPCIONS](#inscripcions)
- [rear categories](#rear-categories)
- [rear clubs](#rear-clubs)
- [rear inscripcions](#rear-inscripcions)
    - [Dia de competició](#dia-de-competició)
    - [Controles de reemplazo](#controles-de-reemplazo)
    - [Parts anul·lades](#parts-anul·lades)
    - [Lliurament de premis](#lliurament-de-premis)
    - [Corredores pendientes](#corredores-pendientes)
    - [Recorreguts](#recorreguts)
- [nar a RECORRIDOS](#nar-a-recorridos)
- [n el camp COMPROBACIÓN DE CÓDIGOS posar-lo a MIXTA](#n-el-camp-comprobación-de-códigos-posar-lo-a-mixta)
    - [i és tot SCORE, en la columna DIVISOR no hi posem res.](#i-és-tot-score-en-la-columna-divisor-no-hi-posem-res)
    - [i hi ha una part línial (els controls surten en color NEGRE) i la darrera és SCORE (els controls surten de color BLAU), en la columna DIVISOR cal posar-hi el codi de control que fa de darrer control del primer tram.](#i-hi-ha-una-part-línial-els-controls-surten-en-color-negre-i-la-darrera-és-score-els-controls-surten-de-color-blau-en-la-columna-divisor-cal-posar-hi-el-codi-de-control-que-fa-de-darrer-control-del-primer-tram)
- [OEScore v.10.3](#oescore-v103)
- [Autodownload](#autodownload)
    - [Add Event](#add-event)
    - [Recorreguts (_Course_)](#recorreguts-_course_)
    - [Controls](#controls)
    - [Penalties](#penalties)
- [OEScore (Rogaines)](#oescore-rogaines)
    - [Configurar les regles](#configurar-les-regles)

<!-- /MarkdownTOC -->




# Introducció 
* Formador: Marc Nicolau
* Data: agost de 2015


# Dispositius basics utilitzats amb el sistema SportIdent
## Bases
### BSF8
* és la reglamentària. Conté un display que permet visualitzar la informació emmagatzemada en la base.

### BSF7-USB
* Permet comunicar qualsevol part del sistema amb l'ordinador:
** programar bases, descarregar pinces, ...

![BSF7-USB](/images/sportident/bsf7-usb.jpg)

## Xip (tarja electrònica)
### Característiques generals
* Es poden mullar.
* Es grava el codi de la base i hh:mm:ss de la base.

### Tipus

#### P-CARD
* Caducaven als 5 anys. 

#### T-CARD
* Les planes, pensades per activitats turístiques.
* Té 20 memòries + check + start + finish.

#### SI5
* Vermella (ja no es fabrica)
* 36 memòries (controls). 
* Velocitat : X. Més lenta que les modernes.
* Només permet curses de 12h.

#### SI6
* Permet gravar el dia de la setmana.
* Curses de fins a 7 dies.
* 60 memòries
* Molt més ràpida que la SI6

#### SI8
* Encara més ràpida.
* 30 memòries
* Preu més econòmic que la SI6.

#### SI9
* 50 memòries.
* Mateixa velocitat que la SI8. 
* Per a corredors d'èlit, Rogaines, etc.

#### SI10
* 128 memòries
* Pensada per a raids
* Preu similar a la SI6 (que ja no es fabrica)

### Funcionament del xip
* Si passen més de 10 segons des de la darrera pinçada, es gasta una altra memòria.

## Altres dispositius
### Bases amb radiofreqüència
### Impressores tèrmiques


# Programar les bases electròniques
* __IMPORTANT__: Totes les bases que no són les de control, números de l'1 al 30.

## Modes de treball
### Control
* Números superiors al 30: del 31 endavant (el 31 correspondria a la fita 1).

### Start
* Com a sortida (número de l'1 al 30)

### Finish
* Meta (número de l'1 al 30)

### Read SI Cards
* Per descarregar la informació de la tarjeta a la base.
* Serveix per a:
  * Entrenaments.
  * Descarregar totes les targes a la base (per si falla el PC).
* La base USB pot tenir qualsevol de les altres funcions.

### Clean
* Neteja

### Check
* Comprova si està buit
* No pita si no està net el xip.

### Printout
* Permet imprimir directament a impressores de paper tèrmic.

### Start with time trigger
* Amb fotocèl·lula

### Finish with time trigger
* Amb fotocèl·lula

## Base SI-Master
* Va juntament amb les targes liles ON-OFF
* 3 funcions (es canvia de mode pinçant successives vegades fins a trobar el que interessa en el display):
  * _Time master_: per posar en hora les altres bases.
  * _Extended master_: per posar en hora i netejar el backup de la base, tot alhora.

## A tenir en compte...
* Per sota de 3.1V de càrrega no utilitzar les bases de control.

## COMPTE AMB LA BASE USB!!
* Si no té prou bateria, cal programar l'hora cada vegada que es desconnecta de l'ordinador (per l'alimentació).
* Si no es reprograma l'hora, les P-CARD i T-CARD no es llegeixen.


## Programari utilitzat
### SI-Config
* Per programar les bases.

#### Modes de treball
* __Direct__: per a programar la base USB.
* __Remote__: per a programar la base de control que hi ha sobre la USB.

#### Opcions del programa

##### READ
* _Working time_: temps de treball (per anar bé, 3 hores, 03:00:00)
* _Auto send_: funció per enviar a Internet o altre dispositiu extern quan es fa la pinçada.
* Icona de la lupa: permet llegir les dades internes de la base de control.

##### WRITE
* _Code no._: número del control
* _Working time_: període de funcionament
* _Set time_: botó independent de l'escriptura, i el que fa és posar en hora la base.
* Botó _WRITE_: configura tots els paràmetres i esborra el backup de la base.
* _Turn off after write_: apaga la base després de reprogramar-la.
* **COMPTE!** Cada vegada que es prem el botó WRITE s'incrementa automàticament el _Code no._ en el programa. Si deixem la mateixa base i tornem a prémer WRITE ens canviarà el _Code no._

##### LOG FILE
* Per veure el que s'ha fet en el programa

##### VIEW
* _Standard_: el més segur i senzill
* _Extended_: apareixen nous camps
  * _Real time clock_
  * _Sprint_: capturar ms per a cèl·lules fotoelèctriques
  * _Stop if backup is full_: s'apaga si s'ha omplert el backup
  * _Extended protocol_

##### View Punch (icona amb rellotge)
* Recuperar les descàrregues de la base USB.
* Ha de funcionar en mode DIRECT.

## SI-Boot
* Per actualitzar el firmware de cada base

# Programa de gestió de curses: OE2010 (v.11)
## Versions
* 500 participants (STANDARD)
* 1000 participants (PRO)
* + de 1000 participants (PRO LARGE).
* Per a les 3 versions hi ha la funció MT (*_multiday_*, per a varis dies): és una llicència addicional i cal comprar-la.

## Introduir la llicència
* CODI: té la forma ...   614B15D45C7ECDEA9D
* Dades de la llicència:
  * Aplicación: OE 2010 (M)--> indica MULTIDAY
  * Tipo: Pro
  * Versión: v.11
  * Caducidad: 09/12/2011 (exemple)

## Gestió de curses de varis dies 
*Apareix un selector amb fletxes (amunt-avall) a la barra d'eines,  on mostra l'etapa: E1, E2, ...
*Els canvis es fan sobre l'etapa activa.

## Crear una CURSA (esdeveniment)
  EVENTO > NUEVO

## CONFIGURACIÓ DE L'ESEDEVENIMENT
 EVENTO > AJUSTES
*Inform. extra 1 i 2: camps informatius extres
*Botó _'Ajustes_':
    *Hora Zero: l'hora a partir de la qual el programa compta que surt el primer corredor.
    **Si ja s'han sortejat les hores i ja s'han publicat, si s'ha de canviar l'hora, per exemple 15min més tard, cal canviar l'hora 0. En els llistats de sortida, continuaríem a l'hora publicada.
    *Toma de tiempos:
    **Utilitzar base de sortida: té sempre preferència sobre l'hora del sorteig
    **Utilitzar base de meta
    *    *No es marca quan es treballa amb cèl·lula fotoelèctrica.
    *    *Modo: "toma de tiempos", "entrada en orden" (per sortida en massa)
## COPIA DE SEGURETAT
*Fer còpia regularment.
*RECOMANAT: en PEN DRIVE o en un altre PC.

## INSCRIPCIONS
#Crear categories
#Crear clubs
#Crear inscripcions
### Crear categories


*Camp nou!! Núm. màx. de corredors: posem el nombre de mapes que tenim, així el programa controla que no es facin més inscripcions que mapes disponibles.
### Crear clubs


*Similar a l'anterior
### Crear corredors


*Camp bloc: permet donar un codi a cada corredor si volem utilitzar-ho a l'hora de fer sortejos, el posi al principi o al final (número gran o baix).

### Plantilles d'informes


 EXTRAS > EDITAR PLANTILLAS

*Permet traspassar plantilles d'un ordinador a un altre.

### Importar


 INSCRIPCIONES > IMPORTAR

*_'ATENCIÓ!! No importar dades si ja s'han publicat hores de sortida, ja que es poden perdre les hores sortejades!!_'

#### Columnes del fitxer d'importació


*No canviar mai el nom de les columnes.
*Id. de base de datos: números llargs
*nc: no classifica
*nº de club: el mateix per a tots els corredors del mateix club
*club: el mateix per a tots els corredors del mateix club. Si s'utilitza, llavors també el camp Ciudad
*ciudad: el mateix per a tots els corredors del mateix club. Si s'utilitza, llavors també el camp Club.
*Nº categoria: número únic per categoria. S'ordenen les categories per aquest codi.
*Corto: Ha de tenir valor si s'utilitza també el Largo.
*Largo: El mateix que el Corto.
*Num1, Num2, Num3: 3 dígits i numèrics.
*Text1, Text2, Text3: limitats a 25 caràcters.
*Alquilado: es posa X (si és llogat)


### Preparar els llistats de sortida: configuració


*Cal separar 4min com a mínim 2 corredors de la mateixa categoria.
*Funciona per caixes de sortida. Se'n poden anar afegint, però no traient. Les caixes de sortida serien aprox. el nombre de circuïts.
    *Les caixes de sortida fan que surti més o menys gent a la vegada al mateix minut.

#### Per categories


 LISTADO DE SALIDA > ORGANIZACIÓN > CATEGORÍAS
* És el millor mètode perquè no s'allarguin massa les hores de sortida, però té el problema que no es compleixi el reglament en el que fa referència als corredors del mateix circuit.
* Hi ha l'informe de comprovació d'errors que t'avisa de problemes o incongruències.

#### Per recorreguts=


 LISTADO DE SALIDA > ORGANIZACIÓN > RECORRIDOS


#### Per clubs


 LISTADO DE SALIDA > ORGANIZACIÓN > CLUBS



### Preparar els llistats de sortida: fer el sorteig


 LISTADO DE SALIDA > SORTEAR > CATEGORIAS

* Es pot fer indicant per quines categories o fer-les totes.
*CAL QUE HI HAGI ELS DORSALS ASSIGNATS ABANS DE SORTEJAR.
    *Es poden assignar des de la mateixa finestra, amb el menú:
 DORSALES

*Separar corredors del mateix club: després de fer el sorteig.
 SEPARAR CLUB

## Dia de competició
### Preparar zona de sortida


*Bases de neteja i control: netejat el backup

### Preparar zona de meta


*Bases de meta: ben sincronitzades

### Llegir xips


 DIA COMPETICION > LEER CHIPS

### Evaluar xips


 DIA COMPETICION > EVALUAR CHIPS

*_'CAS d'UNA SITUACIÓ ANORMAL_'
 Un corredor i tots els de darrera seu tenen el mateix problema en una base es pot agafar la base i comprovar què passa (en cas contrari no es pot comprovar). El corredor pot haver marcat manualment en el mapa el control però això no serveix.

* _'SOLUCIÓ_'
 S'ha d'inserir el control a tots els corredor després de validar que ha fallat la base. Cal fer-ho des del menú ACCIONES->INSERTAR

*Si un corredor ha corregut una categoria que no era la seva, cal fer el següent:
    *Primer cal posar-lo a l'estat "No classifica" (NC), des de la pantalla d'inscripcions.
    *A continuació, canviar-lo la categoria.
    *Finalment, dins "Evaluar Tarjetas" tornar-li a imprimir els parcials.

*Si un corredor és estranger no classifica (NC).

### Moure xip o intercanviar-los


 DIA COMPETICION > EVALUAR CHIPS > ACCIONES > MOVER CHIP
* Cal cercar el dorsal del corredor que s'ha equivocat de xip.
*Indicar el corredor orígen
*Indicar el corredor destí.

## Controles de reemplazo
*Les bases s'han de posar el dia de la cursa.
*Cada fitero ha d'endur-se una tarja SI neta i d'aquesta manera es pot saber quines bases s'han activat.
*Cada fitero s'hauria d'endur 1 o 2 bases de reemplaçament, per si en un determinat moment la base no funciona.
*Amb l'opció: 
 DIA DE COMPETICION > CONTROLES DE REEMPLAZO 
* s'indica a quin control reemplaça un altre:
    *original: el que no hi és
    *de reemplazo: el nou qu ehi posem

## Parts anul·lades
 DIA COMPETICIÓN > PARTES ANULADAS

*Eliminar algun control d'una o vàries categories. Per exemple, control perillós o etc.

*No s'ha d'utilitzar mai si s'ha robat una base! Cal anul·lar la categoria, el recorregut o la cursa.

## Lliurament de premis
 DIA COMPETICIÓN > ENTREGA DE PREMIOS

* Permet saber si ja es poden lliurar premis encara que encara hi hagi corredors en cursa (que ja no tenen opció de podi).

## Corredores pendientes
*Permet saber qui falta per arribar. 
*ULL, que els corredors que no han sortit també hi surten.

*Abans s'ha de fer EVALUAR ESTACIONES SI:
    *El millor és utilitzar la base de NETEJA o la de CHECK.
*#Descarregar picades.
*#_Competidores que no tomaron la salida_: el programa els marca com a corredors que no han sortit.

## Recorreguts
### Categories


*Interessant l'opció _'Categorias indiv._' per indicar en quines categories s'assignen recorreguts individuals als corredors (si és el cas).

### Importar


*El traçador exporta des de l'OCAD (definint molt bé categories i recorreguts) millor en format XML.
*El fitxer exportat, s'importa a SportIdent.

### Configurar recorreguts SCORE i LINIALS barrejats


#Anar a RECORRIDOS
#En el camp COMPROBACIÓN DE CÓDIGOS posar-lo a MIXTA
##Si és tot SCORE, en la columna DIVISOR no hi posem res.
##Si hi ha una part línial (els controls surten en color NEGRE) i la darrera és SCORE (els controls surten de color BLAU), en la columna DIVISOR cal posar-hi el codi de control que fa de darrer control del primer tram.

### HOW-TO'S


*Es pot funcionar sense dorsal?
    *NO, és imprescindible.
*Un corredor descarrega amb un núm SI que no estava registrar. Què fer?
*# Surt un avís, i si sabem el dorsal el posem i es lliga amb les dades del corredor.
*# Si no es té el dorsal, es posa en reserva. Llavors, anem a EVALUAR XIPS>EDITAR>MOVER XIP i es mou cap a la persona que ha de tenir-lo.
*Com es planifiquen les "sortides a la caça"?
*#Cal fer-ho en la modalitat "Varis dies" i dins la finestra de creació de l'esdeveniment, hi ha un checkbox "Sortida a la caça" que cal marcar. Això farà que el darrer dia sigui el de "sortida a la caça" i no faci falta fer el sorteig.


# OEScore v.10.3
*Per organitzar curses score individuals o per equips.


# Autodownload
[[Fitxer:Autodownload.jpg]([Usuari:Mnicolau|Mnicolau]])]

## Add Event
*Event Type: BOF National
*Show Advanced Options
*Autodownload course match: no
*Start time precedence: punching, mass start (prioritat la pinçada amb base sortida, després la sortida en massa)
*Use classes? Sí (amb categories)
*Use start time allocators? No
*Use Race Numbers (dorsals)? si
*Validate start times are unique on each course? No
*Max. Team Size: mida màxima dels equips (l'equip que té més persones). En Rogaines, 5. En Raids, 3.
*Team combination: volem que obligatòriament tots els membres de l'equip pincin la base, que només siguin 1, ...
    *_None_: han de picar tots, però no té en compte l'intèrval entre les picades.
    *_Lazy_: que només pinci un de l'equip.     *
    *_Stric (insist all punch within one minute)_: que passin en menys d'1 minut.
    *_Stric (insist all punch within five minute)_: que passin en menys de 5 minuts.
    *_Stric (insist all punch within fifteen minute)_: que passin en menys de 15 minuts.
*_Earliest punch_: per si és de matí o de tarda.
*_Print splits automatically on download_
*_Show position on splits print and download screens_: mostrar la posició en imprimir (en rogaine no s'ha de posar, només posar-lo en raids)
    *_Splits advertising_: text publicitari.


## Recorreguts (_Course_)
*S'hi pot accedir després d'haver escollit l'esdeveniment. 

### Add course


*_Name_
*_Course checking_
    *_Linear_
    *_Score_: fas les fites que vols (rogaine)
    *_Spanish score_: s'han de fer totes les fites en l'ordre que vols
    *_Linear with butterfly_
    *_Linear with time penalties_
    *_Linear with free order sections_
    *_Linear figure of eight_
*_Score minutes_: temps màxim que es vol donar (en un Rogaine de 6h, 3600min)

## Controls
### Add/Insert control


*_Number_: núm d'ordre
*_Published code_: el codi de la base
*_Control Type_: en funció del tipus de cursa té unes opcions o altres
*_Description_: la descripció textual
*_Electronic code 1..5_: fins a 5 codis de control diferents (per exemple com a controles de reemplazo)
*_Exclude leg from total time?_: per raids, per neutralitzar trams. Exclou des del control anterior que hagi marcat el corredor fins al que estem configurant.
*_Maximum excluded time_:  
*_Team size / num punched_:

## Penalties
### Add Penalty


*_Seconds from_: ?? // ha quedat pendent.


# OEScore (Rogaines)
*A l'hora d'importar les dades amb el full de càlcul, cal assignar hora de sortida a tots els corredors. No és l'hora real, sinó la distància entre hora zero i hora de sortida. 
    *Exemple: si hora zero és 10:00 però la sortida és les 11:00, cal posar com a hora de sortida en el full de càlcul les 1:00:00.


## Configurar les regles
*Serveixen per indicar les penalitzacions.
 Exemple: 0 a 5min (-5), 5 a 10min(-5), 10 a 15min (-10), 15 a 20min(-10), 20 a 25min(-10), 25 a 30min (-10), >30min (desqualificat))

*Cal definir les següents bandes de temps:
[*La Regla de penalització que cal definir és:
[[Fitxer:ReglesRogaine.png]([Fitxer:BandesTemps.png]])]

*Si es creen dos tipus de cursa (6 i 12h per exemple) cal assignar un temps límit diferent a cada categoria.
