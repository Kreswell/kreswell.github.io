---
title: Feed Reader Test
subtitle: Testing reading data from an RSS feed and writing it into a table.
date: 2019-01-15
# js: /js/jquery-1.11.2.min.js
tags: [test]
---

This is a test of getting data from an RSS feed of a published Google spreadsheet and writing it to a table. Updated at 16:49.

<table style="width:100%;max-width:1000%;overflow:auto;" id="runtable"></table>
<table style="width:100%;max-width:1000%;overflow:auto;" id="caltable"></table>
  
<script>
  function displayContent(json) {
    var runstring = "<tr><th>Date</th><th>Run Time</th><th>Distance (km)</th><th>Speed (km/h)</th><th>Steps</th></tr>";  
    var calstring = "<tr><th>Date</th><th>Calorie Goal</th><th>Calories In</th><th>Calories Earned</th><th>Weight</th></tr>";
    var len = json.feed.entry.length;
    for (var i=0; i<len; i++) {
      var rundate = json.feed.entry[i].gsx$date.$t;
      var runtime = json.feed.entry[i].gsx$time.$t;
      var rundist = json.feed.entry[i].gsx$distancekm.$t;
      var runspeed = json.feed.entry[i].gsx$avgspeedkmh.$t;
      var steps = json.feed.entry[i].gsx$steps.$t;
      var calgoal = json.feed.entry[i].gsx$caloriegoal.$t;
      var calin = json.feed.entry[i].gsx$caloriesin.$t;
      var calearned = json.feed.entry[i].gsx$caloriesearned.$t;
      var weight = json.feed.entry[i].gsx$weightlbs.$t;
      var caldeficit = json.feed.entry[i].gsx$deficitwithexercise.$t;
      runstring += "<tr><td>" + rundate + "</td><td>" + runtime + "</td><td>" + rundist + "</td><td>" + runspeed + "</td><td>" + steps + "</td></tr>";
      calstring += "<tr><td>" + "<tr><td>" + rundate + "<tr><td>" + calgoal + "</td><td>" + calin + "</td><td>" + calearned + "</td><td>" + weight + "</td></tr>";
    }
    //runstring += "</table>";
    //calstring += "</table>";
    document.getElementById("runtable").innerHTML = runstring;
    document.getElementById("caltable").innerHTML = calstring;
  }   
</script>
<script src="https://spreadsheets.google.com/feeds/list/1ja2C-UuzQo4i_OrBZe-91Kifm3zWd9pg16xmLlN0Wgs/od6/public/values?alt=json-in-script&amp;callback=displayContent" type="text/javascript"></script>
