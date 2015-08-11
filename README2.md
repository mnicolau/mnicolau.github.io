
# Introducció 
* Formador: Marc Nicolau

* Llicències Autodownload: és una llicència anual.


# Maquinari bàsic utilitzat amb el sistema SportIdent
## Bases
### BSF8


* és la reglamentària. Conté un display que permet visualitzar la informació emmagatzemada en la base.
### BSF7-USB
![BSF7-USB](/images/sportident/bsf7-usb.jpg =100x100)

* permet comunicar qualsevol part del sistema amb l'ordinador: programar bases, descarregar pinces, ...


## Xip (tarja electrònica)
    *Tarja P-CARD (funciona amb el mateix programari que els xips) i T-CARD (les planeres, pensades per activitats turístiques), té 20 memòries + check + start + finish. Les primeres caducaven als 5 anys, ara ja no.
    *Es poden mullar.
    *Es grava el codi de la base i hh:mm:ss de la base.
    *Models:
    **'''SI5:''' vermella (ja no es fabrica)
    *    *36 memòries (controls). Velocitat : X. Més lenta que les modernes.
    *    *Només curses de 12h.
    **'''SI6:'''
    *    * també es permet gravar el dia de la setmana
    *    * Curses de fins a 7 dies.
    *    * 60 memòries
    *    * Molt més ràpid
    **SI8:
    *    *Encara més ràpid.
    *    *30 memòries
    *    *Preu més econòmic.
    **SI9:
    *    *50 memòries
    *    *Mateixa velocitat que la SI8 
    *    *Èlit, Rogaine
    **SI10:
    *    *128 memòries
    *    *Pensada per RAID
    *    *Mateix preu de la SI6 (que ja no es fabrica)
## Funcionament del xip
* Si no passen + de 10seg des de la darrera pinçada, es gasta una altra memòria.

# Altre Maquinari
* Bases amb radiofreqüència
* Impressores tèrmiques


# Programar les bases
* Totes les bases que no són les de control, números de l'1 al 30.

## Control
*Números superiors al 30: del 31 endavant (el 31 correspondria a la balisa 1).
## Start
*Com a sortida (de l'1 al 30)
## Finish
*Meta (de l'1 al 30)

## Read SI Cards
*Descarrega tota la informació de la tarjeta a la base.
*Serveix per:
    *Entrenaments.
    *Descarregar totes les targes a la base (per si falla el PC).
*La base USB pot tenir qualsevol de les altres funcions.

## Clean
*Neteja

## Check
*Comprova si està buit
*No pita si no està net el xip.

## Printout
*Permet imprimir directament a impressores de paper tèrmic.

## Start with time trigger
*Amb fotocèl·lula

## Finish with time trigger
*Amb fotocèl·lula

# Base SI-Master
*Va juntament amb les targes liles ON-OFF
*3 funcions (es canvia de mode pinçant successives vegades fins a trobar el que interessa en el display):
*#Time master: per posar en hora les altres bases
*#Extended master: per posar en hora i netejar el backup de la base, tot alhora.

# Bases de control
*Per sota de 3.1V no utilitzar les bases

# Programari
## SI-Config i SI-Manager
*Per programar les bases: sobretot el SI-Config.

## SI-Boot
*Per actualitzar el firmware de cada base

## Autodownload
*Per RAIDs
*Molt segur i funcional.
*La llicència la pot cedir la FCOC (el fabricant ho permet).


## OE2010 (v.11)
*Versions: 500 participants, 1000 participants (PRO), + de 1000 participants (PRO LARGE).
*Per les 3 versions, hi ha la funció MT (per varis dies): és una llicència addicional i cal comprar-la.

## OEScore v.10.3
*Per organitzar curses score individuals o per equips.

# Programar estacions de control
*Abans s'utilitzava el SI-Manager.

## SI-Config
*Modes de treball:
    *Direct: programes la base USB
    *Remote: programes la base de control que hi ha sobre la USB.

### READ


*Working time: temps de treball (per anar bé, 3 hores, 03:00:00)
*Auto send: funció per enviar a Internet o altre dispositiu extern  quan es fa la pinçada.
*Icona de la lupa: permet llegir les dades internes de la base de control.

### WRITE


* Code no: número del control
* Working time: període de funcionament
* Set time: botó independent de l'escriptura i el que fa és posar en hora la base.
* Bóto WRITE: configura tots els paràmetres i esborra el backup de la base.
*'' Turn off after write'': apaga la base després de reprogramar-la.

*'''COMPTE!''' Cada vegada que es prem el botó WRITE s'incrementa automàticament el Code no en el programa. Si deixem la mateixa base i tornem a prémer WRITE ens canviarà el Code no.


### LOG FILE


* Per veure el que s'ha fet en el programa

### VIEW


*Standard: el més segur i senzill
*Extended: apareixen nous camps
    *Real time clock
    *Sprint: capturar ms per a cèl·lules fotoelèctriques
    *Stop if backup is full: s'apaga si s'ha omplert el backup
    *Extended protocol

### View Punch (icona amb rellotge)


*Recuperar les descàrregues de la base USB.
*Ha de funcionar en mode DIRECT.

### COMPTE AMB LA BASE USB


*Cal programar l'hora cada vegada que es desconnecta de l'ordinador (per l'alimentació).
*Si no es reprograma l'hora les P-CARD i T-CARD no es llegeixen.

# Actualitzar el Firmware de les bases
*S'utilitza el SI-Boot
*En el mateix fitxer que et descarregues ja hi ha els fitxers amb l'actualització del firmware.

# OE 2010 v.11
*Posar llicència
    * CODI: 614B15D45C7ECDEA9D
*Dades de la llicència:
    *Aplicación: OE 2010 (M)--> indica MULTIDAY
    *Tipo: Pro
    *Versión: v.11
    *Caducidad: 09/12/2011

## Multidia
*Spinner de la barra d'eines on apareix l'etapa: E1, E2, ...
*Els canvis es fan sobre l'etapa activa.

## Crear un ESEDEVENIMENT
 EVENTO > NUEVO

## CONFIGURACIÓ DE L'ESEDEVENIMENT
 EVENTO > AJUSTES
*Inform. extra 1 i 2: camps informatius extres
*Botó '''Ajustes''':
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

*'''ATENCIÓ!! No importar dades si ja s'han publicat hores de sortida, ja que es poden perdre les hores sortejades!!'''

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

*'''CAS d'UNA SITUACIÓ ANORMAL'''
 Un corredor i tots els de darrera seu tenen el mateix problema en una base es pot agafar la base i comprovar què passa (en cas contrari no es pot comprovar). El corredor pot haver marcat manualment en el mapa el control però això no serveix.

* '''SOLUCIÓ'''
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
*#''Competidores que no tomaron la salida'': el programa els marca com a corredors que no han sortit.

## Recorreguts
### Categories


*Interessant l'opció '''Categorias indiv.''' per indicar en quines categories s'assignen recorreguts individuals als corredors (si és el cas).

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
    *''None'': han de picar tots, però no té en compte l'intèrval entre les picades.
    *''Lazy'': que només pinci un de l'equip.     *
    *''Stric (insist all punch within one minute)'': que passin en menys d'1 minut.
    *''Stric (insist all punch within five minute)'': que passin en menys de 5 minuts.
    *''Stric (insist all punch within fifteen minute)'': que passin en menys de 15 minuts.
*''Earliest punch'': per si és de matí o de tarda.
*''Print splits automatically on download''
*''Show position on splits print and download screens'': mostrar la posició en imprimir (en rogaine no s'ha de posar, només posar-lo en raids)
    *''Splits advertising'': text publicitari.


## Recorreguts (''Course'')
*S'hi pot accedir després d'haver escollit l'esdeveniment. 

### Add course


*''Name''
*''Course checking''
    *''Linear''
    *''Score'': fas les fites que vols (rogaine)
    *''Spanish score'': s'han de fer totes les fites en l'ordre que vols
    *''Linear with butterfly''
    *''Linear with time penalties''
    *''Linear with free order sections''
    *''Linear figure of eight''
*''Score minutes'': temps màxim que es vol donar (en un Rogaine de 6h, 3600min)

## Controls
### Add/Insert control


*''Number'': núm d'ordre
*''Published code'': el codi de la base
*''Control Type'': en funció del tipus de cursa té unes opcions o altres
*''Description'': la descripció textual
*''Electronic code 1..5'': fins a 5 codis de control diferents (per exemple com a controles de reemplazo)
*''Exclude leg from total time?'': per raids, per neutralitzar trams. Exclou des del control anterior que hagi marcat el corredor fins al que estem configurant.
*''Maximum excluded time'':  
*''Team size / num punched'':

## Penalties
### Add Penalty


*''Seconds from'': ?? // ha quedat pendent.


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
