<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8" />
  <title>WebGIS Langkapura</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Leaflet -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />

  <!-- Custom CSS -->
  <link rel="stylesheet" href="style.css">

  <!-- Geocoder -->
  <link rel="stylesheet" href="https://unpkg.com/leaflet-control-geocoder/dist/Control.Geocoder.css" />
</head>
<body>

<div id="sidebar">
  <h2>WebGIS Langkapura</h2>

  <a class="btn" href="#" id="zoomToArea">Zoom ke Area</a>

  <h3>Daftar Titik</h3>
  <div id="list"></div>
</div>

<div id="map"></div>

<!-- Leaflet JS -->
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<!-- Geocoder JS -->
<script src="https://unpkg.com/leaflet-control-geocoder/dist/Control.Geocoder.js"></script>

<script>
  // INIT MAP
  var map = L.map('map');

  // SEARCH BAR
  L.Control.geocoder({
      defaultMarkGeocode: true,
      placeholder: "Cari lokasi...",
      errorMessage: "Lokasi tidak ditemukan!",
      showResultIcons: true
  }).addTo(map);

  // BASEMAP
  L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      maxZoom: 19
  }).addTo(map);

  var boundsLayer;

  // LOAD POLYGON BATAS WILAYAH
  fetch("api/batas.php")
    .then(r => r.json())
    .then(d => {
      boundsLayer = L.geoJSON(d).addTo(map);
      map.fitBounds(boundsLayer.getBounds());

      // Button zoom
      document.getElementById("zoomToArea").onclick = function(e) {
        e.preventDefault();
        map.fitBounds(boundsLayer.getBounds());
      };
    });

  // LOAD TITIK DIGITASI
  fetch("api/titik.php")
    .then(r => r.json())
    .then(data => {

      var layer = L.geoJSON(data, {
        pointToLayer: (f, latlng) => {
          let icon = L.icon({
              iconUrl: "icons/marker-blue.png",
              shadowUrl: "icons/marker-shadow.png",
              iconSize: [30, 45],
              iconAnchor: [15, 45],
              popupAnchor: [0, -40]
          });

          return L.marker(latlng, { icon: icon });
        },

        onEachFeature: (f, l) => {
          l.bindPopup("<b>" + f.properties.nama + "</b><br>" + f.properties.ket);
        }
      }).addTo(map);

      // LIST TITIK DI SIDEBAR
      var list = document.getElementById("list");
      data.features.forEach(f => {
        var a = document.createElement("a");
        a.href = "#";
        a.className = "data-item";
        a.innerText = f.properties.nama;

        a.onclick = function(e) {
          e.preventDefault();
          var c = f.geometry.coordinates;
          map.setView([c[1], c[0]], 17);
        };

        list.appendChild(a);
      });
    });
</script>

</body>
</html>
