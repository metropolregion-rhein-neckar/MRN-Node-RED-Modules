# Node-RED

<table>
   <thead>
   <tr>
      <th>Kategorie</th>
      <th>Name</th>
      <th>Beschreibung</th>
   </tr>
   </thead>
   <tbody>   
   <tr>
      <td rowspan="8"> <b>CKAN</b></td>
   </tr>
   <tr>
      <td>ckan-dataset-update-prepare</td>
      <td>Updatet je nach Konfiguration das "Zuletzt aktualisiert" von CKAN Ressourcen und das Bezugsjahr (extra im Dataset mit dem Key Jahr) des Datensatzes auf das            aktuelle Datum</td>
   </tr>
    <tr>
      <td>ckan-file-upload-prepare</td>
      <td>Ermöglicht das Erstellen eines neuen CKAN-Datasets</td>
   </tr>
   <tr>
      <td>ckan - upload</td>
      <td>Lädt einen Datensatz auf die angegebene CKAN-Instanz</td>
   </tr>
   <tr>
      <td>ckan - packages - list - csv</td>
      <td>Exportiert alle Datasets einer CKAN-Instanz als CSV</td>
   </tr>
   <tr>
      <td>ckan-file-upload-prepare</td>
      <td>Ermöglicht das Erstellen eines neuen CKAN-Datasets</td>
   </tr>
   <tr>
      <td>ckan-mass-import</td>
      <td>Importiert ein Array von Datasets in eine CKAN-Instanz</td>
   </tr>
   <tr>
      <td>ckan-issue-checker</td>
      <td>Überprüft die Datasets einer CKAN-Instanz auf tote Ressourcen-Links, ob eine Beschreibung vorhanden ist etc.</td>
   </tr>
   <tr>
      <td rowspan="17">Data Request Nodes</td>
   </tr>
   <tr>
      <td>BMVI</td>
      <td>Scraped die Förderlandkarte des BMVIs. Es kann zwischen fertigen und laufenden Projekten unterschieden werden</td>
   </tr>
   <tr>
      <td>DbStations</td>
      <td>Nutzt die DB-API und lädt alle DB-Stationen deutschlandweit herunter</td>
   </tr>
   <tr>
      <td>Fairteiler</td>
      <td>Nutzt die Foodsharing API und lädt je nach Auswahl die aktuellen Foodbaskets oder die Standorte der Fairtailer herunter. Zusätzlich wird die Fairtailer Webseite gescraped um weitere Informationen (Beschreibung etc.) zu den einzelnen Fairtailern/Foodbaskets zu erhalten</td>
   </tr>
    <tr>
      <td>Freifunk</td>
      <td>Nutzt die Freifunk API um die Freifunk Standorte innerhalb einer ausgewählten BBox abzufragen</td>
   </tr>
   <tr>
      <td>goingElectric</td>
      <td>Nutzt die goingElectric-API und eine BBox um Ladesäulenstandorte innerhalb der gewählten Region herunterzuladen. Es kann zusätzlich nach Fast-Charger gefiltert werden</td>
   </tr>
   <tr>
      <td>Ladesäulenregister</td>
      <td>Nutzt den ESRI-Feature-Server und lädt alle im Ladesäulenregister verzeichneten Standorte herunter. Es kann zusätzlich nach Fast-Charger gefiltert werden</td>
   </tr>
   <tr>
      <td>LDI</td>
      <td>Nutzt die LuftdatenInfo API, um die Messwerte aller Sensoren innerhalb einer BBox zu einem bestimmten Merkmal herunterzuladen. Es kann zwischen Temperatur, Luftdruck, PM10 etc. gewählt werden</td>
   </tr>
   <tr>
      <td>UBA (MRN ONLY)</td>
      <td>Nutzt die API des Umweltbundesamtes, um die Messwerte von Sensoren innerhalb der MRN abzufragen (Kann bei Bedarf erweitert werden, damit nicht nur Stationen innerhalb der MRN abgefragt werden)</td>
   </tr>
   <tr>
      <td>Opensense</td>
      <td>Nutzt die OpenSense API, um die Messwerte aller Sensoren innerhalb einer BBox zu einem bestimmten Merkmal herunterzuladen. Es kann zwischen Temperatur, Luftdruck, PM10 etc. gewählt werden</td>
   </tr>
    <tr>
      <td>LoRaWan</td>
      <td>Frägt die im TheThinghsNetwork vorhandenen Gateways innerhalb einer gegbenen Region (Mittelpunkt + Radius) ab</td>
   </tr>
   <tr>
      <td>mundraub</td>
      <td>Frägt die von der Community eingetragenen Mundraubstandorte inklusive Beschreibung ab.</td>
   </tr>
   <tr>
      <td>Nextbike (MRN ONLY)</td>
      <td>Nutzt die Nextbike API und frägt die Daten zu allen Stationen innerhalb der MRN ab, kann bei Bedarf flexibilisiert werden (nicht nur MRN)</td>
   </tr>
   <tr>
      <td>OoklaSpeedTest</td>
      <td>Requestet die Ergebnisse des aktuellen Ookla-Speed-Test und schneidet diese auf eine BBox zu. Es kann zwischen mobilem Internet und dem Internet „aus der     Leitung“ differenziert werden</td>
   </tr>
   <tr>
      <td>recup</td>
      <td>Frägt alle Recup-Standorte ab</td>
   </tr>
   <tr>
      <td>refill</td>
      <td>Frägt alle Refill-Standorte über die KarteVonMorgen API ab</td>
   </tr>
    <tr>
      <td>UVP</td>
      <td>Requestet die Ergebnisse der Umweltverträglichkeitsprüfung</td>
   </tr>
    <tr>
      <td rowspan="9">GeoJSON</td>
   </tr>
   <tr>
    <td>geocoder</td>
    <td>Geocoded ein GeoJSON und ersetzt dessen Geometry (Addresse --> Koordinaten)</td>
    </tr>
    <tr>
        <td>merge-geojson</td>
        <td>Concatenates die Features von 2 GeoJSONs, oder joined die Properties von 2 Featuren, wenn ein gegebenes Property in beiden Featuren gleich ist.</td>
     </tr>
     <tr>
        <td>geojson-values-filter</td>
        <td>Filtert die Features eines GeoJSONs abhängig von den Property-Values der Features oder deren Distanz zueinander. Es kann bspw. Nach Outliern (letztes Quantil), nach leeren Properties oder nach speziellen Property-Werten gefiltert werden </td>
     </tr>
     <tr>
        <td>geojson-properties-filter</td>
        <td>Filtert die Properties aller Features eines GeoJSONs</td>
     </tr>
     <tr>
        <td>geojson-properties-renamer</td>
        <td>Renamed die Property-Keys der Features eines GeoJSONs</td>
     </tr>
     <tr>
        <td>geojson-spatial-within</td>
        <td>Verscheidet ein Intersecting GeoJSON und ein Source GeoJSON. Alle Features des Intersecting GeoJSONs, welche innerhalb des Source GeoJSONs liegen, werden beibehalten. Bei LineStrings und Polygonen werden die Geometrien auf die Source Layer geclipped.</td>
     </tr>
     <tr>
        <td>geojson-to-centroids</td>
        <td>Ersetzt die Geometry eines jeden Features eines GeoJSONs durch den Centroid des Features</td>
     </tr>
     <tr>
        <td>geojson-value-offset</td>
        <td>Kann benutzt werden, um die Properties eines GeoJSON-Features zu verrechnen (Grundrechenoperationen). Es können entweder 2 Properties eines Features oder 1 Property und eine Konstante miteinander verrechnet werden</td>
     </tr>
     <tr>
        <td>geojson-to-gpkg</td>
        <td>Transformiert ein GeoJSON in ein Geopackage</td>
     </tr>
     <tr>
        <td>Geoserver</td>
        <td>geoserver-publish</td>
        <td>Pusht ein Geopackage auf einen angegebenen Arbeitsbereich eines Geoservers</td>
     </tr>
     <tr>
        <td rowspan="2">OpenStreetMap  </td>
     </tr>
     <tr>
        <td>osm-overpass-download</td>
        <td>Nutzt die overpass-API, um OSM Daten herunterzuladen. Kann nach Tags filtern und Filtertags können verkettet werden. </td>
     </tr>
     <tr>
        <td>osm-overpass-to-geojson</td>
        <td>Wandelt das OSM-XML in ein GeoJSON um</td>
     </tr>
   </tbody>
</table>


