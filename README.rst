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


