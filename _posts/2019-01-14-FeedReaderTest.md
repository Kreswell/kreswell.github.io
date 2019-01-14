---
title: Feed Reader Test
subtitle: Testing reading data from an RSS feed and writing it into a table.
date: 2019-01-14
js: /js/jquery-1.11.2.min.js
tags: [test]
---

This is a test of getting data from an RSS feed of a published Google spreadsheet and writing it to a table. Updated 17:24 CT.

<table style="width:100%" id="tbl">
  <tr>
    <th>Date</th>
    <th>Run Time</th>
    <th>Distance (km)</th>
    <th>Speed (km/h)</th>
  </tr>
</table>
<p id="errMsg">No error message printed.</p>

<script>  
  var feedUrl = https://spreadsheets.google.com/feeds/list/1ja2C-UuzQo4i_OrBZe-91Kifm3zWd9pg16xmLlN0Wgs/default/public/values;
    fetch(feedUrl).then((res) => {
      res.text().then((xmlTxt) => {
        var domParser = new DOMParser();
        let doc = domParser.parseFromString(xmlTxt, 'text/xml');
        doc.querySelectorAll('entry').forEach((entry) => {
          var newrow = table.insertRow(1);
          var newcell0 = newrow.insertCell(0);
          var newcell1 = newrow.insertCell(1);
          var newcell2 = newrow.insertCell(2);
          var newcell3 = newrow.insertCell(3);
          var runtime = entry.querySelector('gsx:time').textContent;
          var rundist = entry.querySelector('gsx:distancekm').textContent;
  	  var runspeed = 60*rundist/runtime;
        newcell0.innerHTML = entry.querySelector("gsx:date").textContent;
        newcell1.innerHTML = runtime;
        newcell2.innerHTML = rundist;
        newcell3.innerHTML = runspeed;
      });
    });
  }).catch(() => errMsg.innerHTML = 'Error in fetching the website');
</script>
