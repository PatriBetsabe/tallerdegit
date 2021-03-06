###############################
Introducció al reStructuredText
###############################

El reStructuredText (*rst* en breu) és un format de presentació de documents que ofereix un bon
balanç entre la llegibilitat directa dels continguts i la possibilitat de processar automàticament
aquests continguts per a convertir-los en altres formats.

Amb una cerca ràpida per la Web, hi trobem multitud de recursos per a aprendre a fer servir aquest
format, així com eines per a processar documents en rst. Un dels més recomenables és `Quick
reStructuredText <http://docutils.sourceforge.net/docs/user/rst/quickref.html>`_ on cada element
apareix en codi rst i, al costat, com podria ser representat típicament.

Comencem
========

Veiem una breu introducció als elements més bàsics, que ens permetran comença a realitzar els
nostres primers documents en aquest format.

.. note::

   Insisteixo, és una *breu* introducció. Encara que aprendràs el necessari per la majoria de les
   necessitats bàsiques, si vols més opcions, et caldrà estudiar una mica més!

Permet-me que et demostri com és de fàcil entendre un document rst, deixant que sigui ell qui faci
la seva presentació. És qüestió de temps (poc) que et sembli natural llegir directament en aquest
format!

.. code-block:: none

        ##################
        Títol del document
        ##################

        Comencem
        ========

        La línia anterior correspon a un títol de secció principal. Fixa't com
        el símbol = subratlla *tota* la paraula sense passar-se. Altrament els
        processadors automàtics ho considerarien un error. Fixa't també com,
        aquest altre paràgraf apareix separat una línia del subratllat del títol
        de secció.  Aquesta separació de, com a mínim una línia, és necessària.

        Aquest text, en canvi, correspon al cost de text del document.

        Si vull iniciar un paràgraf nou, en tinc prou amb separar-lo de
        l'anterior amb una o més línies en blanc. Si en poso de més no importa.
        Si no deixo línia en blanc com en aquest cas totes aquestes línies
        apareixeran en el mateix paràgraf.

        Aquesta és una subsecció
        ------------------------

        Podem fer diferents nivells de seccions. En aquest cas, aquesta secció
        es consideraria dins de la secció *Comencem*.

        Podríem haver fet servir el guió '-' per la secció *Comencem* i l'igual
        '=' per aquesta subsecció.  La relació entre secció i subsecció s'hagués
        mantingut. No obstant, típicament l'ordre que trobarem és =, -, ^, '. Si
        el teu document necessita més de quatre nivells, considera si és la
        estructuració més idònia!

        Aquesta és una altra subsecció
        ------------------------------

        Aquesta nova subsecció estaria també dins de la secció *Comencem* i a
        continuació de l'anterior.

        És important estructurar coherentment els continguts nostres documents
        en seccions. Entre d'altres coses, les eines automàtiques ens poden
        generar taules de continguts, enllaços a partir del nom de la secció,
        presentacions diferents (ex. un títol de primer nivell amb una lletra
        més gran que la del segon), etc.

        Estils bàsics
        =============

        Negretes i cursives
        -------------------

        A banda de l'estructura del document, sovint necessitarem remarcar
        altres parts del document de manera especial. Habitualment això
        s'aconsegueix posant en negreta o cursiva una o més paraules especials.

        En rst, posarem en cursiva una paraula, o grup de paraules,
        envoltant-les entre asteriscs. Per exemple, *aquestes paraules*
        apareixeran en cursiva si convertim aquest document a format odt (del
        libreoffice).

        Si volem ressaltar una paraula en negreta, ho farem envoltant-la entre
        **dos** asteriscs (com és el cas de la paraula 'dos' anterior)

        Alguns editors, ja preparats pel format rst, fins i tot podrien realment
        mostrar-te en negreta o cursiva aquestes paraules! En tot cas, amb el
        temps no et serà necessari. Com a la pel·lícula *Matrix*, ja podràs
        llegir el codi del document directament.

        Codi
        ----

        Fins ara, les paraules del text que hem introduït apareixen separades
        per un espai. Podria ser més d'un espai         com en aquest cas, però
        els processadors automàtics els ignorarien. Això és un problema quan el
        que volem és que aparegui el text tal i com l'hem introduït (per
        exemple, el codi d'un programa)

        En aquests casos, finalitzarem la línia anterior amb dos cops el símbol
        ':'

        Per exemple, considera aquest codi ::

            if (a == b) {
                printf("iguals\n");
            }

        També podem indicar els dobles dos punts en una línia per separat.

        ::

            if (a == b) {
                printf("iguals!\n");
            }

        Alguns processadors de rst, poden fins i tot acceptar que se'ls indiqui
        el tipus de codi. Per exemple, Sphinx (el generador de documentació amb
        el que es processen aquests continguts) accepta la notació:

        .. code-block:: c

            if (a == b) {
                printf("iguals\n");
            }

        En aquest darrer cas, el processador del document podria fins i tot
        distingir amb colors els diferents elements del codi (*sintax
        highlighting*).

        En tots tres casos, fixa't que el codi apareix tabulat respecte l'inici
        de la línia que conté el doble dos punts.

        Enllaços
        --------

        Un altre element típic són els enllaços (*links*) a pàgines web,
        recursos, etc. Els podem fer fàcilment així: `google <http://google.com>`_.

        Fixa't en que el text es troba entre cometes inclinades '`', l'adreça
        apareix entre angles '<>', i en el guió baix del final.

        També podem fer referència a les nostres seccions, com per exemple
        `Comencem`_ faria enllaçar amb el títol de la primera secció d'aquest
        document!

        Llistes
        -------

        Un altre element típic són les llistes. En tenim bàsicament de dos
        tipus:

        * numerades

        * no numerades

        Els dos tipus anteriors, col·locats darrera d'un asterisc + espai, ja
        són una llista (no numerada en aquest cas) En comptes de l'asterisc hi
        podríem fer servir altres caràcters com ara el guió '-'.

        En cas que la vulguem numerada, per exemple, per indicar un ordre, podem
        fer servir directament els números, com a la següent recepta:

        1. agafa el pollastre

        2. treu-li les plomes

        3. posa'l a la cassola amb la resta d'ingredients

        4. engega el foc i espera fins que estigui fet

        A banda dels números seguits de punt, podem fer servir per exemple, lletres i parèntesis. Com ara

        1) Aquest element té tres subelements

           a. primer

           b. segon

           c. tercer

        2) Aquest no en té cap de subelement

        taules
        ------

        Sovint els nostres documents requeriran representar la informació de
        manera tabulada. El format rst ens ofereix diferents maneres de composar
        una taula, la més senzilla, potser seria la següent:

        ==============================      =======
        Veí/veïna                           pis
        ==============================      =======
        Sra. Josefa Ramos Granados          1er 1ra
        Sr. Vicent Carallot i Gripau        1er 2na
        ==============================      =======

        Tot i que al principi pot ser una mica incòmode escriure aquestes
        taules, no em negaràs que és fàcil de llegir tal qual? A més, a la
        llarga, aprendràs trucs per construir-les i modificar-les.

        imatges
        -------

        De vegades voldrem incloure imatges als nostres documents. Evidentment
        aquestes imatges no es veuran en el text, però si escollim un bon nom
        ens farem una idea clara del que contenen.

        Una manera fàcil és:

        .. image:: imatges/lamevafoto.png

Processem
=========

Una de les eines més habituals per a processar els documents rst, és ``docutils``.

Per exemple, si
el document de la secció anterior estigués en un fitxer anomenat intro.rst, el podríem convertir a
format libreoffice amb la comanda:

.. code-block:: sh

    $ rst2odt intro.rst intro.odt

El ``docutils`` és un paquet amb diferents utilitats de conversió (ex. rst2odt, rst2html,
rst2pdf…) que segurament trobaràs empaquetat en la teva distribució GNU/Linux (com ara Debian) o
disponible des de `sourceforge <http://docutils.sourceforge.net/>`_

Una altra coneguda utilitat és `pandoc <http://pandoc.org/>`_ que permet convertir entre diferents
formats incloent rst.

