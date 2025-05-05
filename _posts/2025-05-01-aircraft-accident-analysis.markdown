---
layout: home
title:  "Aircraft Accident Analysis: A Data Story"
date:   2025-05-01
categories: jekyll update
---
<h1 style="color:rgb(107, 142, 202);">Introduction </h1>

<p style="text-align: justify;">
Flying is one of the safest modes of transportation today, but this hasn't always been the case. Over the years, aviation has undergone numerous improvements in safety, technology, and regulations. To better understand how aviation safety has evolved, this project analyzes historical data on aircraft accidents.

<br>
<br>
By examining real-world accident records from 1948 to the present, we explore various trends in crash frequency, operator types, and damage severity. Through a series of interactive visualizations, we can better grasp the factors influencing aviation safety, uncovering patterns in crash incidents across decades.

<br>
<br>
The figure below, "Number of Aircraft Accidents per Year," visualizes the trend in aircraft accidents over time. As you can see, there was a significant spike in crashes during the mid-20th century, particularly around the late 1940s and early 1950s which can be easily interpreted as the result of accidents linked to World War II. This dramatic increase coincides with the expansion of air travel, followed by improvements in aircraft technology and safety standards that led to a decline in accidents over the years. 
<p style="text-align: justify;">

</p>
<iframe src="{{ '/assets/plotly_html/crashes_per_year.html' | relative_url }}"
        width="100%"
        height="500"
        style="border:none;"
        scrolling="no"
        title="Interactive chart showing number of aircraft accidents per year">
</iframe>
<p style="text-align: justify;">
</p>

<h1 style="color:rgb(107, 142, 202);">Fatalities Over Time</h1>
Using this classification, we created a series of interactive line charts showing how crash counts per year differ by operator category. 
When we shifted our focus from the number of accidents to the actual number of people involved—charting the fatalities per year—the story took on another dimension. You can immediately see the chart is dominated by that huge peak around 1944, really showing the scale of loss during World War II. Afterwards, even as air travel became more common for everyone, the fatality numbers unfortunately remained high and fluctuated quite a bit for many years. We spotted some notably tragic spikes sticking out, like around 1972 and 1985.
<br>
<br>
That year, 1972, is sadly remembered as one of the deadliest ever for flying. It wasn't just one single event, but a whole string of awful crashes involving large passenger jets like the Soviet Ilyushin Il-62, the British Trident, and American DC-8s and L-1011s. For instance, there was a massive Aeroflot crash near Moscow where 174 people died when the plane went down on approach, a BEA Trident jet stalled and crashed right after takeoff from London killing 118, and an Eastern Airlines L-1011 wide-body jet crashed in Florida partly because the crew got distracted by a warning light – and these were just some of the major accidents making 1972 such a terrible peak.
<br>
<br>
Then, 1985 stands out partly because of some other huge, separate disasters, including the horrific Japan Airlines Flight 123 crash (the deadliest single-plane accident ever with over 500 deaths) and the bombing of Air India Flight 182 over the Atlantic. What was really striking for us, though, is seeing the clear downward trend in recent decades. This positive direction underscores just how far safety measures have come, making flying much safer today compared to those earlier, tougher times.
<br>
<br>
Lastly, we also noticed that smaller bump upwards in the fatality numbers right around 2013 to 2015 on the chart. It's nowhere near the huge peaks from the earlier decades, but it definitely stands out against the general downward slope we see in more recent times. When we looked into those specific years, we found that 2014 especially was sadly marked by some really major, high-profile, and unusual air tragedies involving large passenger planes. That was the year Malaysia Airlines faced two terrible events: MH370, the Boeing 777 that mysteriously disappeared, and MH17, another Boeing 777 that was tragically shot down over Ukraine. Then, 2015 added to this period's toll with awful events like the Germanwings Airbus A320 crash in the Alps, deliberately caused by the co-pilot, and the Metrojet Airbus A321 crash in Egypt, thought to be caused by a bomb. So, it seems that while overall safety from typical accidents (like mechanical failure or standard pilot error) might have still been improving, these specific, terrible events – including deliberate acts like the shoot-down and the pilot suicide – tragically pushed the total number of lives lost higher for that short period, creating that noticeable bump we see on our chart.
</p>
<iframe src="{{ '/assets/plotly_html/fatalities_per_year.html' | relative_url }}"
        width="100%"
        height="500"
        style="border:none;"
        scrolling="no"
        title="Interactive chart showing total fatalities in aircraft accidents per year">
</iframe>

<br>

<h1 style="color:rgb(107, 142, 202);">Accidents by Operator Category Over Time</h1>
<p style="text-align: justify;">
    Every crash record in our dataset includes an operator, which could be a military body, a commercial airline, or an individual private pilot. We grouped these into four categories: </p>
<ul>
    <li>Civilian/Commercial </li>
    <li>Military </li>
    <li>Private </li>
    <li>Other/Unknown </li>
  </ul>

This is where the data really started telling different stories for us. Instead of just looking at one big trend, we wondered how different kinds of flying compared over the years. So, we split the accidents out by who was operating the aircraft: Military, Civilian/Commercial (like the airlines we all fly on), Private pilots, and everyone else kinda lumped into 'Other/Unknown'. The charts below show the accident counts per year for each group, and wow, the patterns we found are really distinct! You can clearly see that huge spike and then sharp drop for Military flights right after World War II. That's a totally different story compared to the airlines, where accidents first increased as flying became more common, but thankfully have been decreasing for decades as planes and safety rules got better.
<br>
<br>
The 'Private' chart was really interesting for us. Look how the accidents jumped way up around 2019-2020, then quickly fell again! Why right then? Well, the big COVID travel changes didn't really start until 2020, so that doesn't fully explain the jump starting in 2019. But the 2020 part fits the story – private flying apparently boomed when airlines faced restrictions. So maybe more flights (perhaps with newer or 'rustier' pilots?) meant more accidents for a while in our data? It could also just be something unusual about the data we used for those years, or maybe how our code grouped the 'Private' operators. It's still a bit of a puzzle for us, but definitely a unique pattern we noticed!"


<iframe src="{{ '/assets/bokeh_html/operator_accidents.html' | relative_url }}"
        width="150%"
        height="1000"  
        style="border:none;"
        scrolling="yes"
        title="Interactive faceted chart showing accidents per year by operator category">
</iframe>

<p style="text-align: justify;">
This visualization helps compare the trends across different types of aviation operations throughout the decades analyzed.
</p>
<h1 style="color:rgb(107, 142, 202);"> A Look at the Top Operators by Accident Count  </h1>

<br>
To get another angle on the data, we decided to rank the specific operators with the most recorded accidents across the whole time period. This bar chart shows the top 15, and it really paints a picture heavily influenced by history, especially wartime. It's impossible to miss the United States Army Air Force (USAAF) at the very top – their massive number of accidents reflects the sheer scale of flying operations during World War II. Following them are other major military air arms like the modern United States Air Force (USAF) and Britain's Royal Air Force (RAF), which also makes sense given their historical activity levels.
<br>
<br>
We were also initially surprised to see the United States Navy so high up, thinking mostly of ships! But then we remembered that navies operate huge air forces too – think about all the planes and helicopters flying from aircraft carriers and naval bases. Naval aviation has its own unique challenges, like landing on moving ships, which unfortunately means more opportunities for accidents compared to some other types of flying. So, their high ranking reflects their significant role in aviation history. Further down the list, we start seeing the big, familiar names of commercial airlines like American, United, and Delta, which have flown countless miles over many decades. And, of course, the 'private' and 'Unknown' categories pop up again, reminding us of the diversity in the data.
</p>
![Number of Aircraft Accidents per Year]({{ "/images/top15operators.png" | relative_url }})

<br>
<br>

Military aviation historically reports the highest number of accidents, especially before the 1990s. Civilian aviation, while more prominent today, shows a steady decrease in major accidents since the early 2000s. 
<br>


<h1 style="color:rgb(107, 142, 202);"> Aviation Eras: Propellers to Jets </h1>

<p style="text-align: justify;"> To explore how aviation safety has evolved with technology, we divided the timeline into three broad eras: </p>

<ul>
    <li>Propeller Era (before 1960)  </li>
    <li>Early Jet Era (1960–1979)  </li>
    <li>Modern Jet Era (1980–present)   </li>
  </ul>

<p style="text-align: justify;">
In each era, we analyzed the severity of aircraft damage by operator type using a faceted bar chart. 
<br>
<br>
[Plotly Bar Chart: Damage Severity Distribution by Era and Operator Type] 
<br>
<br>
In the Modern Era, civilian aircraft accidents are far less likely to result in a total loss (write-off) compared to earlier decades. In contrast, military operations maintain a relatively high proportion of serious damage cases, likely due to the nature of their missions. </p>
<br>


<h1 style="color:rgb(107, 142, 202);"> How Serious Were These Accidents? </h1>

<p style="text-align: justify;"> The dataset includes labels for damage level, such as: </p>

<ul>
    <li>sub (substantial damage) </li>
    <li>w/o (write-off) </li>
    <li>min, non, mis, unk, and Unknown  </li>
  </ul>

<p style="text-align: justify;">
We visualized how these labels are distributed across operators and time. 
<br>
<br>
 [Bokeh Dashboard: Survivable Major Accidents (Fatalities ≤ 1)] 
<br>
<br>
This dashboard focuses on low-fatality incidents and reveals interesting survivability patterns based on aircraft type, operator, and damage level. 
<br>
<br>
Most survivable accidents involve substantial damage rather than total write-offs. The dashboard shows that certain operator types, especially civilian/commercial, have higher survivability rates in more recent decades. </p>
<br>


<h1 style="color:rgb(107, 142, 202);"> What We Learned </h1>

<p style="text-align: justify;"> 
<ul>
    <li>Military accidents have consistently occurred more often but also align with high-risk operational contexts.  </li>
    <li>Civilian safety has improved drastically, especially after 1980.  </li>
    <li>Damage outcomes have shifted from write-offs to more survivable outcomes in recent decades.   </li>
    <li>Survivability in low-fatality crashes correlates with less severe damage and more robust safety protocols.   </li>
  </ul>




<style>
  /* Style the references section */
  .references-list ul {
    padding-left: 20px; /* Adjust indentation if needed */
  }
  .references-list li {
    font-size: 0.9em; /* Make the list item text slightly smaller */
    margin-bottom: 0.5em; /* Add a little space between items */
    color: #555; /* Slightly lighter text color, common in Minima */
  }
  .references-list li a {
    color: rgb(107, 142, 202); /* Link color to match heading */
    text-decoration: none; /* Optional: remove underline */
  }
  .references-list li a:hover {
    text-decoration: underline; /* Add underline on hover */
  }
</style>

<div class="references-list">
  <h2 style="color: rgb(107, 142, 202);">References</h2> <ul>
    <li>
      <strong>Aeroflot Flight 217 (1972):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Ilyushin Il-62 CCCP-86671 Moskva-Sheremetyevo Airport (SVO)</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=19721013-1" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=19721013-1</a>
    </li>
    <li>
      <strong>BEA Flight 548 (1972):</strong> Wikipedia contributors. (2025, April 28). <em>British European Airways Flight 548</em>. Wikipedia. <a href="https://en.wikipedia.org/wiki/British_European_Airways_Flight_548" target="_blank" rel="noopener noreferrer">https://en.wikipedia.org/wiki/British_European_Airways_Flight_548</a>
    </li>
    <li>
      <strong>Eastern Air Lines Flight 401 (1972):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Lockheed L-1011-385-1 TriStar 1 N310EA Everglades, FL</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=19721229-1" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=19721229-1</a>
    </li>
    <li>
      <strong>Japan Airlines Flight 123 (1985):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Boeing 747SR-46 JA8119 Ueno</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=19850812-1" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=19850812-1</a>
    </li>
    <li>
      <strong>Air India Flight 182 (1985):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Boeing 747-237B VT-EFO Cork, Ireland</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=19850623-0" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=19850623-0</a>
    </li>
    <li>
      <strong>Malaysia Airlines Flight 370 (2014):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Boeing 777-2H6ER 9M-MRO Indian Ocean</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=20140308-0" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=20140308-0</a>
    </li>
    <li>
      <strong>Malaysia Airlines Flight 17 (2014):</strong> Dutch Safety Board. (n.d.). <em>Crash of Malaysia Airlines flight MH17</em>. Retrieved May 5, 2025, from <a href="https://www.onderzoeksraad.nl/en/page/14941/crash-malaysia-airlines-flight-mh17" target="_blank" rel="noopener noreferrer">https://www.onderzoeksraad.nl/en/page/14941/crash-malaysia-airlines-flight-mh17</a>
    </li>
    <li>
      <strong>Germanwings Flight 9525 (2015):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Airbus A320-211 D-AIPX Prads-Haute-Bléone</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=20150324-0" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=20150324-0</a>
    </li>
    <li>
      <strong>Metrojet Flight 9268 (2015):</strong> Aviation Safety Network. (n.d.). <em>ASN Aircraft accident Airbus A321-231 EI-ETJ Hasna, North Sinai</em>. Retrieved May 5, 2025, from <a href="https://aviation-safety.net/database/record.php?id=20151031-0" target="_blank" rel="noopener noreferrer">https://aviation-safety.net/database/record.php?id=20151031-0</a>
    </li>
  </ul>
</div>




</p>

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
