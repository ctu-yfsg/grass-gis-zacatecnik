.. index::
   pair: dotazování; prostorové dotazy
   single: v.select

Prostorové dotazy
-----------------

Prostorové dotazy, tj. výběr geoprvků na základě jejich prostorových
vztahů, zajišťuje modul :grasscmd:`v.select` (:menuselection:`Vector
--> Feature selection --> Select by another map`). Nativně tento modul
podporuje pouze jeden prostorový operátor:

* *overlap* - geoprvky se částečně či úplně překrývají

Pokud je GRASS zkompilován s podporou knihovny `GEOS
<http://trac.osgeo.org/geos>`_, tak je množina prostorových operátorů
rozšířena o:

* *equals* - geoprvky jsou totožné
* *disjoint* - geoprvky jsou prostorově různé 
* *intersects* - geoprvky se prostorově protínají
* *touches* - geoprvky se prostorově dotýkají
* *crosses* - geoprvky se kříží
* *within* - geoprvek je prostorově lokalizován uvnitř jiného geoprvku
* *contains* - geoprvek je prostorově obsažen v jiném geoprvku
* *overlaps* - geoprvky se prostorově překrývají
* *relate* - obecný prostorový vztah definovaný jako vztahová matice

Knihovna GEOS implementuje prostorové operátory dle :wikipedia:`OGC`
specifikace `Simple Features Access
<http://www.opengeospatial.org/standards/sfa>`_ více o této
specifikaci `zde <http://geo.fsv.cvut.cz/~gin/uzpd/uzpd.pdf#18>`_.

.. rubric:: :secnotoc:`Příklad`

Výběr komunikací (vektorová mapa :map:`streets_wake`), které kříží (v
tomto případě může použít např. prostorový operátor *crosses*)
železnice (vektorová mapa :map:`railroads`).

.. youtube:: teA-x-vmXYc

             Prostorový dotaz - výběr komunikací, které kříží železnice
