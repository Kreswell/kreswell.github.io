---
title: Feed Reader Test
subtitle: Testing reading data from an RSS feed and writing it into a table.
date: 2019-01-15
js: /js/jquery-1.11.2.min.js
tags: [test]
---

This is a test of getting data from an RSS feed of a published Google spreadsheet and writing it to a table. Updated 11:58 CT.

<div style="width:100%" id="sheet">
  <tr>
    <th>Date</th>
    <th>Run Time</th>
    <th>Distance (km)</th>
    <th>Speed (km/h)</th>
  </tr>
</div>
  
<script>
  function displayContent(json) {
	  var string = "<table><tr><th>Date</th><th>Run Time</th><th>Distance (km)</th><th>Speed (km/h)</th></tr>";      
    var len = json.feed.entry.length;
    for (var i=0; i<len; i++) {
      var date = json.feed.entry[i].gsx$date.$t;
      var runtime = json.feed.entry[i].gsx$time.$t;
      var rundist = json.feed.entry[i].gsx$distancekm.$t;
      var runspeed = 60*rundist/runtime;
		  string += '<tr><td>' + date + '</td><td>' + runtime + '</td><td>' + rundist + '</td><td>' + runspeed + '</td></tr>';
    }
	  string += "</table>";
	  document.getElementById("sheet").innerHTML = string;
  }   
</script>
<script>
<script src="http://spreadsheets.google.com/feeds/list/1ja2C-UuzQo4i_OrBZe-91Kifm3zWd9pg16xmLlN0Wgs/od6/public/values?alt=json-in-script&amp;callback=displayContent" type="text/javascript"></script>
</script>
