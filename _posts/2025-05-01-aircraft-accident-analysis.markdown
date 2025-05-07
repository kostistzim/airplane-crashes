---
layout: home
title:  "Aircraft Accident Analysis: A Data Story"
date:   2025-05-01
categories: jekyll update
---
<h1 style="font-weight: bold; color:rgb(107, 142, 202);">Introduction </h1>

<p style="text-align: justify;">
Flying is one of the safest forms of transport today, but it hasn't always been that way. The history of aviation safety is one of tragedy, resilience and incredible progress. Over the years, aviation has undergone numerous improvements in safety, technology and regulation that have made air travel what it is today.  
<br> 
<br> 

By examining historical data on aircraft accidents from 1948 to the present, this project reveals how aviation safety has evolved. We'll look at trends in accident frequency, types of operator and severity of damage, and how these patterns have shaped the skies we fly in today.  
<br> 
<br> 

Through a series of interactive visualisations, we delve deep into the data to understand the factors that have influenced aviation safety and the lessons we can learn from past incidents.The figure below, 'Number of aircraft accidents per year', visualises the trend in aircraft accidents over time. As you can see, there was a significant increase in the number of accidents in the middle of the 20th century, particularly in the late 1940s and early 1950s. This increase is largely due to accidents associated with the Second World War and the rapid expansion of air travel. After this period, however, advances in aircraft technology and safety regulations contributed to a steady decline in the number of accidents, demonstrating the continuous improvement in aviation safety.  </p> 



<iframe src="{{ '/assets/plotly_html/crashes_per_year.html' | relative_url }}"
        width="100%"
        height="500"
        style="border:none;"
        scrolling="no"
        title="Interactive chart showing number of aircraft accidents per year">
</iframe>
<p style="text-align: center;"> 

  <b><span style="color: rgb(88, 117, 169);">Figure 1</span></b>: Number of Aircraft Accidents per Year 

</p> 



<br>

<h1 style="font-weight: bold; color:rgb(107, 142, 202);">Historical Trends</h1>
<p style="text-align: justify;">
When we move from examining the number of accidents to analysing the actual number of fatalities over time, the story of aviation safety takes on a more sombre and personal dimension. The graph below, entitled Total Fatalities in Aircraft Accidents per Year, visually captures this evolution, highlighting the peaks and valleys of human loss over the decades. 
<br>
<br>
One of the most striking features of the graph is the massive spike in fatalities around 1944. This peak reflects the devastating loss of life during the Second World War, when military aviation operations were at their most intense and many lives were lost in both combat and non-combat accidents. This tragic period underlines the risks associated with early aviation, particularly when military and commercial operations overlapped in such an unprecedented way. 
<br>
<br>
After the Second World War, as air travel expanded worldwide, the number of fatalities remained high, with some notable fluctuations over the decades. The 1970s and 1980s saw a number of disastrous years for aviation. However, despite these challenges, the general trend over time has been a steady decline in fatalities, thanks to improvements in aircraft technology, safety protocols and regulatory oversight. This positive trend underlines how far aviation has come, with the number of fatalities per flight falling significantly in recent decades. 
</p>

<br>
<h3 style="color:rgb(107, 142, 202);">Fatalities and High-Impact Years</h3>
<p style="text-align: justify;">
While the general trend has been a reduction in the number of fatalities, certain years stand out for catastrophic accidents that caused significant loss of life. For example, 1972 is remembered as one of the deadliest years in aviation history. It wasn't a single crash, but a series of tragic accidents involving large passenger aircraft such as the Soviet Ilyushin Il-62, the British Trident and the American DC-8 and L-1011. A major event that year was the crash of an Aeroflot flight near Moscow, where 174 people died when the plane crashed on approach. A BEA Trident jet also stalled shortly after take-off from London, killing 118 people, while an Eastern Airlines L-1011 crashed in Florida, partly because the crew was distracted by a warning light. 
<br>
<br>
Another grim milestone came in 1985 with the devastating crash of Japan Airlines Flight 123, which remains the deadliest single aircraft accident in history, claiming more than 500 lives. In the same year, Air India Flight 182 was bombed over the Atlantic, adding to the year's high death toll. 
<br>
<br>
Despite these tragic outliers, the most striking trend is the decline in fatalities over recent decades. There was, however, a brief increase in fatalities between 2013 and 2015. While these numbers are small compared to the peaks of the mid-20th century, they are marked by high-profile events. In 2014, Malaysia Airlines experienced two tragic incidents: the mysterious disappearance of MH370 and the downing of MH17 over Ukraine. The following year, 2015, saw the crash of the Germanwings A320, deliberately caused by a co-pilot, and the bombing of Metrojet flight 9268 in Egypt. While these incidents temporarily interrupted the overall downward trend in fatalities, they highlight that despite such outliers, aviation safety continues to improve, with fatalities per flight still much lower than in the past. 
</p>
<iframe src="{{ '/assets/plotly_html/fatalities_per_year.html' | relative_url }}"
        width="100%"
        height="500"
        style="border:none;"
        scrolling="no"
        title="Interactive chart showing total fatalities in aircraft accidents per year">
</iframe>

<p style="text-align: center;"> 

  <b><span style="color: rgb(88, 117, 169);">Figure 2</span></b>: Total Fatalities Aircraft Accidents per Year

</p> 
<br>
<br>

<h1 style="font-weight: bold; color:rgb(107, 142, 202);">Accidents by Operator Category: A Closer Look </h1>
<p style="text-align: justify;">
  Each crash in our dataset is categorised by its operator, which could be a military organisation, a commercial airline, a private pilot or an unknown entity. We divide the accidents into four categories:  </p>
<ul>
    <li>Civilian/Commercial </li>
    <li>Military </li>
    <li>Private </li>
    <li>Other/Unknown </li>
  </ul>

<p style="text-align: justify;">
Examining accident trends in different types of aviation operations provides fascinating insights. When accidents are broken down by category of operator, clear patterns emerge that highlight the evolution of aviation safety. 
<br>
<br>
Military aviation shows a sharp spike in accidents just after the Second World War, reflecting the wartime surge in air operations, followed by a steep decline as activity tapered off after the war. In contrast, civil/commercial aviation, such as today's airlines, initially saw an increase in accidents as air travel became more widespread. Over the decades, however, the number of accidents has steadily declined, thanks to advances in aircraft technology and improved safety protocols. 
<br>
<br>
The graph for private aviation shows a fascinating anomaly. Between 2019 and 2020, there is a noticeable spike in accidents, followed by a rapid decline. This increase doesn't coincide with the start of the COVID-19 restrictions, raising questions: did private aviation surge when commercial airlines were grounded? Could the increase in flights, possibly by newer or less experienced pilots, have contributed to this spike? While the cause remains uncertain, it's a compelling pattern worthy of further investigation. 
<br>
<br>
The Other/Unknown category adds further context to the data, representing a mix of unidentified operators that do not follow a clear trend, but still provide valuable insight. 
<br>
<br>
This visualisation allows a clear comparison of accident trends between military, commercial and private aviation, shedding light on how safety has evolved in these different sectors.</p> 

<iframe src="{{ '/assets/bokeh_html/operator_accidents.html' | relative_url }}" 
    width="110%" 
    height="1000" 
    style="border: none;" 
    scrolling="yes" 
    title="Interactive faceted chart showing accidents per year by operator category">
  </iframe>

<p style="text-align: center;"> 

  <b><span style="color: rgb(88, 117, 169);">Figure 3</span></b>: Accidents by Operator per Year

</p> 

<br>
<br>
<h1 style="font-weight: bold; color:rgb(107, 142, 202);"> Top Operators by Number of Accidents</h1>
<p style="text-align: justify;">
The bar chart below ranks the top 15 operators with the most recorded accidents, providing a perspective shaped by history - particularly wartime activity. 
<br>
<br>
At the top of the list is the United States Army Air Force (USAAF), reflecting the scale of operations during the Second World War, where many accidents occurred as part of massive military air campaigns. Close behind are other major air forces such as the modern United States Air Force (USAF) and the Royal Air Force (RAF), which also had high levels of activity during and after the war. 
<br>
<br>
Surprisingly, the US Navy also ranks highly. Known for its fleet of ships, the Navy also operates an extensive air force, with planes and helicopters flying from aircraft carriers and naval bases. The unique challenges of naval aviation - such as landing on moving ships - naturally increase the likelihood of accidents, placing the Navy high on the list. 
<br>
<br>
Further down the list are commercial airlines such as American, United and Delta. While these airlines have flown millions of miles over decades, their accident rates have dropped significantly in recent years due to advances in technology and safety protocols. 
<br>
<br>
Finally, the Private and Unknown categories highlight the diverse range of operators in the dataset, providing a broader picture of aviation safety across different sectors. </p> 

![Number of Aircraft Accidents per Year]({{ "/images/top15operators.png" | relative_url }})

<p style="text-align: center;"> 

  <b><span style="color: rgb(88, 117, 169);">Figure 4</span></b>: Top 15 Operators by Number of Accidents

</p> 


<br>
<br>

<h1 style="font-weight: bold; color:rgb(107, 142, 202);"> Aviation Eras: The Impact of Evolving Technology </h1>

<p style="text-align: justify;"> As we’ve seen, the number of aircraft accidents and fatalities has declined significantly over time. But another equally important dimension of aviation safety is how severe accidents are when they do happen, and this has also changed dramatically with advances in technology. 
<br>
<br>
To explore this, we divided our data into three major aviation eras:  </p>

<ul>
    <li>Propeller Era (before 1960)  </li>
    <li>Early Jet Era (1960–1979)  </li>
    <li>Modern Jet Era (1980–present)   </li>
  </ul>

<p style="text-align: justify;">
Each era marks a significant stage in the development of aviation technology, from early piston-driven aircraft to the introduction of commercial jets and, more recently, highly automated and electronically controlled airliners.
<br>
<br>
In the visualisation below, we look at the types of damage sustained in aircraft accidents across these three eras. The severity of each accident is categorised into four groups: Write-off (total destruction of the aircraft), Substantial, Minor, and Unknown/None. Each category is colour-coded and grouped by era, allowing us to track how the nature of accident outcomes has shifted over time. 

<br>
<br>
In the Propeller Era, accidents were overwhelmingly severe. The majority resulted in the complete destruction of the aircraft, reflecting both the fragility of early designs and the limited safety protocols of the time. These were aircraft built without modern materials, flying without real-time weather systems, and often without any formalised emergency procedures. 
<br>
<br>
As we enter the Jet Age, the story begins to shift. Aircraft became more robust, systems more redundant, and regulations more strict. During the Early Jet Era, there is a noticeable increase in survivable incidents, accidents that no longer resulted in total loss, but instead ended in substantial or minor damage. These improvements were largely driven by innovations in navigation, improved airport infrastructure, and the introduction of cockpit procedures like crew resource management. 
<br>
<br>
By the Modern Jet Era, this transformation becomes even more pronounced. While accidents have become less frequent overall, the accidents that do occur are more likely to be survivable. This is due to a combination of technological advances, such as enhanced structural design, better crashworthiness, improved fire suppression systems, and real-time monitoring, as well as regulatory changes, pilot training reforms, and global coordination on aviation safety standards. 
<br>
<br>
The evolution of accident severity is a powerful indicator of progress. It shows that aviation safety is not only about reducing the number of incidents, it’s also about reducing the consequences when things go wrong. The chart below provides a clear visual representation of this shift, underlining how far the industry has come in designing aircraft and systems that protect both passengers and crew. 
 </p>

<iframe src="{{ '/assets/plotly_html/aircraft_accident_severity.html' | relative_url }}"
        width="200%"
        height="600"
        style="border:none;"
        scrolling="no"
        title="Interactive chart showing total fatalities in aircraft accidents per year">
</iframe>
<p style="text-align: center;"> 

  <b><span style="color: rgb(88, 117, 169);">Figure 5</span></b>: Aircraft Accident Severity by Era 

</p> 

<br>
<br>
<style>
  /* Style the references section */
  .references-list ul {
    padding-left: 20px; /* Adjust indentation if needed */
  }
  .references-list li {
    font-size: 0.9em; /* Make the list item text slightly smaller */
    margin-bottom: 0.5em; /* Add a little space between items */
    color: #555; /* Slightly lighter text color, common in Minima */
    text-align: justify;
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
  <strong>Airplane Crash & Fatalities (1948–Present):</strong>
  Kaggle. (n.d.). Retrieved May 5, 2025, from <a href="https://www.kaggle.com/datasets/themuneeb99/airplane-crash-and-fatalities-1948present/data" target="_blank" rel="noopener noreferrer">https://www.kaggle.com/datasets/themuneeb99/airplane-crash-and-fatalities-1948present/data</a>
</li>
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



[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
