<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8" />
  <style>
    html, body, #map { height: 100%; width: 100%; margin: 0; padding: 0; }
    img { max-width: 100px; margin: 4px; display: inline-block; }
    h3 { margin: 0; }
  </style>
  <script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAyzahoIMckGWx_NAAilSiN30mED1kbD7Y&libraries=places"></script>
</head>
<body>
  <div id="map"></div>
  <script>
    let map;

    window.addEventListener("message", (event) => {
      const locations = event.data;
      initMap();
      geocodeAndAddMarkers(locations);
    });

    function initMap() {
      map = new google.maps.Map(document.getElementById("map"), {
        zoom: 11,
        center: { lat: 40.782, lng: -73.246 } // Brentwood default
      });
    }

    function geocodeAndAddMarkers(locations) {
      const geocoder = new google.maps.Geocoder();

      locations.forEach(loc => {
        geocoder.geocode({ address: loc.address }, (results, status) => {
          if (status === "OK") {
            const marker = new google.maps.Marker({
              map: map,
              position: results[0].geometry.location,
              title: loc.title
            });

            const infoWindow = new google.maps.InfoWindow({
              content: `
                <div style="max-width:250px;">
                  <h3>${loc.title}</h3>
                  <p><strong>Date:</strong> ${loc.date || 'N/A'}<br>
                  <strong>Time:</strong> ${loc.time || 'N/A'}</p>
                  <p>${loc.description || ''}</p>
                  ${loc.images.map(img => `<img src="${img}" />`).join('')}
                  ${loc.link ? `<p><a href="${loc.link}" target="_blank">More Info</a></p>` : ''}
                </div>`
            });

            marker.addListener('click', () => infoWindow.open(map, marker));
          } else {
            console.error("Geocode failed for:", loc.address, status);
          }
        });
      });
    }
  </script>
</body>
</html>
