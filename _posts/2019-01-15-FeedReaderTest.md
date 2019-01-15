---
title: 30-30-30 Log
subtitle: A single page for logging my "30-30-30" fitness plan progress.
date: 2019-01-15
tags: [30-30-30, programming]
---

This is a page I'm setting up for logging and displaying my progress on my "30-30-30" fitness plan. I plan to update it regularly. 

## Exercise Data

<table style="width:100%;overflow:auto;" id="runtable"></table>

## Calorie Data

<table style="width:100%;overflow:auto;" id="caltable"></table>

## Comments

- 1/15/2019: I've figured out how to pull data into this page straight from a Google spreadsheet! So some of the stuff will be updated automatically when I enter data there. There's still a bunch of over-analysis I want to do, so my next step is to figure out how to get that working. I'm not sure how I'm going to do that. It will have to either be by coding it in javascript, doing it in Google Sheets and pulling it over, or getting some code in another language (python or R, probably) running within the page (if that's possible).
  
<script>
  function displayContent(json) {
    var runstring = "<tr><th>Date</th><th>Run Time</th><th>Distance (km)</th><th>Speed (km/h)</th><th>Steps</th></tr>";  
    var calstring = "<tr><th>Date</th><th>Calorie Goal</th><th>Calories In</th><th>Calories Earned</th><th>Calorie Deficit</th><th>Weight</th></tr>";
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
      runstring += "<tr><td nowrap>" + rundate + "</td><td>" + runtime + "</td><td>" + rundist + "</td><td>" + runspeed + "</td><td>" + steps + "</td></tr>";
      calstring += "<tr><td nowrap>" + rundate + "</td><td>" + calgoal + "</td><td>" + calin + "</td><td>" + calearned + "</td><td>" + caldeficit + "</td><td>" + weight + "</td></tr>";
    }
    //runstring += "</table>";
    //calstring += "</table>";
    document.getElementById("runtable").innerHTML = runstring;
    document.getElementById("caltable").innerHTML = calstring;
  }   
</script>
<script src="https://spreadsheets.google.com/feeds/list/1ja2C-UuzQo4i_OrBZe-91Kifm3zWd9pg16xmLlN0Wgs/od6/public/values?alt=json-in-script&amp;callback=displayContent" type="text/javascript"></script>
