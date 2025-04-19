---
permalink: /readings/sunday/
title: "Sunday's Reflection"
layout: single
# author_profile: true
---
<hr>
<script>
function receivedUniversalisItem(thing)
{var where=document.getElementById("Universalis_" + thing);
 if (where)
   where.style.display="block";
 };
function setUniversalisElement(thing,text)
{var where=document.getElementById("Universalis_" + thing);
 if (where)
   where.innerHTML=text;
 };
function universalisCallback(data)
{for (var thing in data)
  {receivedUniversalisItem(thing);
   var d=data[thing];
   if (typeof d != "object")
     {setUniversalisElement(thing,d)
	  }
	else
	 {for (var t in d)
	   {var dd=d[t];
	    setUniversalisElement(thing + "." + t,dd);
		}
	 }
   }
}
!function(d,id,region,day){function yyyymmdd(day){var now=new Date();var delta=day==7?7-now.getDay():0;var when=new Date(now.getTime()+86400000*delta);return (1900+when.getYear())*10000+(1+when.getMonth())*100+when.getDate();};var js,fjs=d.getElementsByTagName('script')[0];if(!d.getElementById(id)){js=d.createElement('script');js.id=id;js.src=document.location.protocol+'//universalis.com/' + (region==""?region:region+"/") + yyyymmdd(day) + '/jsonpmass.js?callback=universalisCallback';fjs.parentNode.insertBefore(js,fjs);}}(document, 'universalis-js',
/* CUSTOMIZATION: the local calendar

  Insert the name of the local calendar: for instance, "Europe.England.Westminster". For the General Calendar, use an empty string: just "".
  */

"Europe.England.Westminster"
, // Leave this comma here: it really is needed!

/* CUSTOMIZATION: which day do you want?
   Insert 1 for today's readings.
   Insert 7 for next Sunday's readings.
   */

7
);
</script>

<div style="display:flex;justify-content: space-around;align-items: center;">
  <div id="Universalis_day"></div>
  <div style="font-size::16px;" id="Universalis_date"></div>
</div>

<!-- <p id="Universalis_date" style="font-size:small; float:right;"></p>
<p style=" float:left;" class="text-center" id="Universalis_day"></p> -->


<h3 class="text-center">First Reading</h3>

<p style="font-size:16px;" class="text-center" id="Universalis_Mass_R1.source"></p>

<p class="" id="Universalis_Mass_R1.text"></p>

<h3 class="text-center">Psalm</h3>
<p style="font-size:16px;" class="text-center" id="Universalis_Mass_Ps.source"></p>
<p id="Universalis_Mass_Ps.text"></p>

<!-- The Second Readings are wrapped in a <div> block which is set not to display. 
      If there is a Second Reading today then the receivedUniversalisItem() function will make this block visible. -->

<div id="Universalis_Mass_R2" style="display:none">
<h3 class="text-center">Second Reading</h3>
<p style="font-size:16px;" class="text-center" id="Universalis_Mass_R2.source"></p>
<p id="Universalis_Mass_R2.text"></p>
</div>

<h3 class="text-center">Gospel</h3>
<p style="font-size:16px;" class="text-center" id="Universalis_Mass_G.source"></p>
<p id="Universalis_Mass_G.text">
<!-- We have included a link here. When data arrive from Universalis, the link will be replaced by the text of today's Gospel.
     It is good practice to have a link like this so that someone who has Javascript turned off will not be faced with a completely blank page.
     -->
<a style="font-size:14px" href="http://www.universalis.com/mass.html">Click here for today's Mass readings from Universalis</a>
</p>


<p style="font-size:12px" id="Universalis_copyright.text"></p>