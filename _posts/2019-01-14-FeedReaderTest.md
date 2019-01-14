---
title: Feed Reader Test
subtitle: Testing reading data from an RSS feed and writing it into a table.
date: 2019-01-14
js: /js/jquery-1.11.2.min.js
tags: [test]
---

This is a test of getting data from an RSS feed of a published Google spreadsheet and writing it to a table. Updated 17:18 CT.

<table style="width:100%" id="tbl"></table>

<script>
  var table = document.getElementById("tbl");
  var row = table.insertRow(0);
  var cell0 = row.insertCell(0);
  var cell1 = row.insertCell(1);
  var cell2 = row.insertCell(2);
  var cell3 = row.insertCell(3);

  cell0.innerHTML = "Date";
  cell1.innerHTML = "Run Time";
  cell2.innerHTML = "Distance (km)";
  cell3.innerHTML = "Speed (km/h)";
  
  //var feedUrl = https://spreadsheets.google.com/feeds/list/1ja2C-UuzQo4i_OrBZe-91Kifm3zWd9pg16xmLlN0Wgs/default/public/values;
  //  fetch(feedUrl).then((res) => {
  //    res.text().then((xmlTxt) => {
  //      var domParser = new DOMParser();
  //      let doc = domParser.parseFromString(xmlTxt, 'text/xml');
  //      doc.querySelectorAll('entry').forEach((entry) => {
  //        var newrow = table.insertRow(1);
  //        var newcell0 = newrow.insertCell(0);
  //        var newcell1 = newrow.insertCell(1);
  //        var newcell2 = newrow.insertCell(2);
  //        var newcell3 = newrow.insertCell(3);
  //        var runtime = entry.querySelector('gsx:time').textContent;
  //        var rundist = entry.querySelector('gsx:distancekm').textContent;
  //	  var runspeed = 60*rundist/runtime;
  //      newcell0.innerHTML = entry.querySelector("gsx:date").textContent;
  //      newcell1.innerHTML = runtime;
  //      newcell2.innerHTML = rundist;
  //      newcell3.innerHTML = runspeed;
  //    });
  //  });
  //});
</script>
