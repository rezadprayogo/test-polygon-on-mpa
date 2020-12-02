# test-polygon-on-mpa
<!DOCTYPE html>
<html>
  <head>

    <style type="text/css">
      html { height: 100% }
      body { height: 100%; margin: 0; padding: 0 }
      #map-canvas { height: 100%; width:100%; }
    </style>
    <script type="text/javascript"
      src="https://maps.googleapis.com/maps/api/js?v=3.exp&sensor=false">
    </script>
    
  </head>
  <body>
    <div id="map-canvas"/>

    <script type="text/javascript">
      function initialize() {
        var mapOptions = {
          center: new google.maps.LatLng(-6.346988,106.852888),
          zoom: 18
        };
  
var map = new google.maps.Map(document.getElementById("map-canvas"),mapOptions);
 
  var A=new google.maps.LatLng(-6.346939314782444, 106.85289013631362);
  var B=new google.maps.LatLng(-6.347017288513295, 106.85285660868426);
  var C=new google.maps.LatLng(-6.347062606593203, 106.8529390866164);
  var D=new google.maps.LatLng(-6.346987965071215, 106.85298133141313);
  var E=new google.maps.LatLng(-6.346931257903701, 106.85295573194256);
  <?php
   $rute_terbang1=[A,B,C,D,E];
   $rute_terbang2=[A,B,C,D];

if ($rute_terbang1>$rute_terbang2) {
  var rute_terbang1=[A,B,C,D,E];}
  else { var $rute_terbang2=[A,B,C,D];}

?>
  
  var poly=new google.maps.Polygon({
  path:(rute_terbang1,rute_terbang2),
  strokeColor:"#0000FF",
  strokeOpacity:0.8,
  strokeWeight:2,
  fillColor:"#0000FF",
  fillOpacity:0.4
  });

  poly.setMap(map);
      }
      google.maps.event.addDomListener(window,'load',initialize);
      
    </script>
  </body>
</html>
