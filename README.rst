============================
consulta-resultado-electoral
============================

Esquemas para pasar de formato ancho fijo a CSV los archivos de la BASE DE DATOS
DE RESULTADOS ELECTORALES del Ministerio del Interior de España

Prerrequisitos
--------------

1. Descargar las definiciones de los archvivos de datos de formato fijo del
   Ministerio.

2. Instalar utilidades csvkit

Uso
---

1. Descarga archivo con las fuentes

::

    wget http://www.infoelectoral.mir.es/docxl/apliext/07200906_MESA.zip

2. Extrae los datos

::

    unzip 07200906_MESA.zip -d datos

3. Convierte a CSV

::

    in2csv -s 01xxaamm.csv datos/01070906.DAT > datos/01070906.csv

Más información
---------------

En el archivo de explicación de la base de datos, se puede leer la explicación
de los códigos utilizados para nombrar a los archivos:

    El nombre de los ficheros es el siguiente:

    ::
        nnxxaamm.dat

    donde 

    - nn = Código identificativo del tipo de fichero. Estos códigos son los siguientes:

        - 01 = Fichero de control.
        - 02 = Fichero de identificación del proceso electoral.
        - 03 = Fichero de candidaturas.
        - 04 = Fichero de candidatos.
        - 05 = Fichero de datos globales de ámbito municipal.
        - 06 = Fichero de datos de candidaturas de ámbito municipal.
        - 07 = Fichero de datos globales de ámbito superior al municipio.
        - 08 = Fichero de datos de candidaturas de ámbito superior al municipio.
        - 09 = Fichero de datos globales de mesas.
        - 10 = Fichero de datos de candidaturas de mesas.
        - 11 = Fichero de datos globales de municipios menores de 250 habitantes (en elecciones municipales).
        - 12 = Fichero de datos de candidaturas de municipios menores de 250 habitantes (en elecciones municipales).

    - xx = Tipo de proceso electoral:

        - 01 = Referéndum.
        - 02 = Elecciones al Congreso de los Diputados.
        - 03 = Elecciones al Senado.
        - 04 = Elecciones Municipales.
        - 05 = Elecciones Autonómicas.
        - 06 = Elecciones a Cabildos Insulares.
        - 07 = Elecciones al Parlamento Europeo.
        - 10 = Elecciones a Partidos Judiciales y Diputaciones Provinciales.
        - 15 = Elecciones a Juntas Generales.

    - aa = Dos últimas cifras del año de celebración del proceso electoral.

    - mm = Dos dígitos correspondientes al mes de celebración del proceso electoral.

    - dat = Es siempre la extensión de los ficheros.

