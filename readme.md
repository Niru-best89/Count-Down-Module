# Count Down Module
This module is for showcasing upcoming event timer. This module is meant to be used with a Coded HubSpot Template.
The following resources were used:
1.Custom Modules

A demo of this in action can be seen on https://preview.hs-sites.com/_hcms/preview/template/multi?is_buffered_template_layout=true&portalId=2474026&tc_deviceCategory=undefined&template_layout_id=13430734727&updated=1568621668416

## How to use this module
After coding your custom template, your best use with this module inside of pre-defined Flexible Column area. An example of this is below:

  <div class="text-center countDown">
  <div class="">
  <span class='countDate' src='{{ module.countdown_date|datetimeformat('%Y/%m/%d') }}'></span>  
  <div class="dateCount noListStyle">
        <ul>
       <li class='ib'><span id="days"></span> days</li>
       <li class='ib'><span id="hours"></span> Hours</li>
    <li class='ib'><span id="minutes"></span> Minutes</li>
         <li class='ib'><span id="seconds"></span> Seconds</li>
       </ul>
     </div>
     </div>
  
 
  Once you have this code in your custom module with some javascript for it given below:
  
  // js
  <pre>
var date = $('.countDate').attr('src');
const second = 1000,
      minute = second * 60,
      hour = minute * 60,
      day = hour * 24;
       let countDown = new Date(date).getTime(),
        x = setInterval(function() {
        let now = new Date().getTime(),
        distance = countDown - now;
        document.getElementById('days').innerText = Math.floor(distance / (day)),
        document.getElementById('hours').innerText = Math.floor((distance % (day)) / (hour)),
        document.getElementById('minutes').innerText = Math.floor((distance % (hour)) / (minute)),
        document.getElementById('seconds').innerText = Math.floor((distance % (minute)) / second);  }, second)
            
   </pre>

  You can use this module and place it at any point of your page design ....
checkout the below link to know how to create custom modules   https://knowledge.hubspot.com/articles/kcs_article/cos-general/create-and-edit-modules for example

Below link is a vedio where this shows how to work with this module:
<p><img src="https://drive.google.com/open?id=1gh9y_rkmwRl99mBE3LV1hqp44LXkteQu"></p>
https://drive.google.com/open?id=1gh9y_rkmwRl99mBE3LV1hqp44LXkteQu
https://drive.google.com/open?id=1o36lfj1RF-CGYRR3OVNDCYOQWnBlE4A8
https://drive.google.com/open?id=1upLMZdsYr_4KgxXEOQVPbb1ICdLBMc0n

https://www.loom.com/share/0fc08026b64f4f46aa0e10351d15e591


