---
title: Feed Reader Test
subtitle: Testing reading data from an RSS feed and writing it into a table.
date: 2019-01-14
tags: [test]
---

This is a test of getting data from an RSS feed of a published Google spreadsheet and writing it to a table.

<table style="width:100%" id="tbl"></table>

<div id="testzone"></div>

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

  //var rownum = 0;
  var feed = "https://spreadsheets.google.com/feeds/list/1ja2C-UuzQo4i_OrBZe-91Kifm3zWd9pg16xmLlN0Wgs/default/public/values";
	  $.ajax(feed, 
    {
		  accepts:
    {
			xml:"application/rss+xml"
		},
		dataType:"xml",
		success:function(data) 
    {
			$(data).find("entry").each(function () 
      { 
				var el = $(this);
        var newrow = table.insertRow(1);
        var newcell0 = newrow.insertCell(0);
        var newcell1 = newrow.insertCell(1);
        var newcell2 = newrow.insertCell(2);
        var newcell3 = newrow.insertCell(3);
        var runtime = el.find("gsx:time").text();
	console.log(runtime);
	testzone.innerHTML = "<p>" + runtime + "</p>";
        var rundist = el.find("gsx:distancekm").text();
	console.log(rundist);
	testzone.innerHTML = "<p>" + rundist + "</p>";
	var runspeed = 60*rundist/runtime;
	console.log(runspeed);
	testzone.innerHTML = "<p>" + runspeed + "</p>";
        newcell0.innerHTML = el.find("gsx:date").text();
        newcell1.innerHTML = runtime;
        newcell2.innerHTML = rundist;
        newcell3.innerHTML = runspeed;
			});
		}	
	});
</script>
