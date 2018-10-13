---
ID: 121
post_title: Criminal-(draft)
author: weibo huang
post_excerpt: ""
layout: page
permalink: >
  https://findcaringarea.ga/index.php/criminal-2/
published: true
post_date: 2018-10-03 08:19:45
---
[wbcr_php_snippet id="689"]

<script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyB8ezYx7QnuyzmUeBPAoYlSLFYcYm9pAC8&libraries=places&callback=initMap" 
          type="text/javascript"></script>


<script>
 var locations = [
["Melbourne", -37.8150, 144.946014, 0],
["Ballarat",-37.5662, 143.8496, 1],
["Bendigo", -36.757786, 144.278702, 2],
["Geelong", -38.14711, 144.36069, 3],
["Hume", -37.5780, 144.7357, 4],
["Latrobe", -37.69686, 144.053177, 6],
["North-West", -34.206841, 142.136490, 7],
["Shepparton", -36.3805, 145.3987, 8], 
["Warrnambool",-38.38176, 142.48799, 9]];
var map = new google.maps.Map(document.getElementById('map'), 
							  {zoom: 7,
							   center: new google.maps.LatLng(-37.8150, 144.946014)});
var infowindow = new google.maps.InfoWindow();
var marker, i;
for (i = 0; i < locations.length; i++) {  
	marker = new google.maps.Marker({
		position: new google.maps.LatLng(locations[i][1], locations[i][2]),
        map: map
	  });
          google.maps.event.addListener(marker, 'click', (function(marker, i) {
        return function() {
          infowindow.setContent(locations[i][0]);
          infowindow.open(map, marker);
        }
		  })(marker, i));}
</script>
<h2><span style="font-size: 24pt;">Select the Year </span></h2>
<table>
<tbody>
<tr>
<td>
<ul id="menu">
 	<li><button id="year2" class="butto1" onclick=getvalue1(this) value="2016">2016</button></li>
 	<li><button id="year3" class="butto1" onclick=getvalue1(this) value="2021">2021</button></li>
 	<li><button id="year4" class="butto1" onclick=getvalue1(this) value="2026">2026</button></li>
 	<li><button id="year5" class="butto1" onclick=getvalue1(this) value="2031">2031</button></li>
</ul>
</td>
</tr>
</tbody>
</table>

<h2><span style="font-size: 24pt;">Choose the Area you are interested in</span></h2>
<table>
<tbody>
<tr>
<td>
<ul id="menu">
 	<li><button id="btn1" class="butto1" onclick=getvalue(this) value="Melbourne">Melbourne</button></li>
 	<li><button id="btn2" class="butto1" onclick=getvalue(this) value="Ballarat">Ballarat</button></li>
 	<li><button id="btn3" class="butto1" onclick=getvalue(this) value="Bendigo">Bendigo</button></li>
 	<li><button id="btn4" class="butto1" onclick=getvalue(this) value="Geelong">Geelong</button></li>
 	<li><button id="btn5" class="butto1" onclick=getvalue(this) value="Hume">Hume</button></li>
 	<li><button id="btn6" class="butto1" onclick=getvalue(this) value="Latrobe">Latrobe</button></li>
 	<li><button id="btn7" class="butto1" onclick=getvalue(this) value="North-West">NorthWest</button></li>
 	<li><button id="btn8" class="butto1" onclick=getvalue(this) value="Shepparton">Shepparton</button></li>
 	<li><button id="btn9" class="butto1" onclick=getvalue(this) value="Warrnambool">Warrnambool</button></li>
</ul>
</td>
</tr>
</tbody>
</table>

<div id="hidenone", style="display:none";>
<h2><span style="font-size: 24pt;">Select the age group</span></h2>
<table>
<tbody>
<tr>
<td>
<ul id="menu">
 	<li><button id="Age1" class="button3" onclick=getvalue2(this) value="65-69">65-69</button></li>
 	<li><button id="Age2" class="button3" onclick=getvalue2(this) value="70-74">70-74</button></li>
 	<li><button id="Age3" class="button3" onclick=getvalue2(this) value="75-79">75-79</button></li>
</ul>
</td>
</tr>
</tbody>
</table>
</div>

<div id="title" style="font-size:30px;">Population</div>
<div id="map"  style="width: 100%; height: 500px;"></div>