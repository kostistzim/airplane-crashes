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
The figure below, "Number of Aircraft Accidents per Year," visualizes the trend in aircraft accidents over time. As you can see, there was a significant spike in crashes during the mid-20th century, particularly around the late 1940s and early 1950s. This dramatic increase coincides with the expansion of air travel, followed by improvements in aircraft technology and safety standards that led to a decline in accidents over the years. </p>

![Number of Aircraft Accidents per Year](/images/Number_of_Aircraft_Accidents_per_Year.jpeg)


<br>


<h1 style="color:rgb(107, 142, 202);"> Who's Responsible for the Aircraft? </h1>

<p style="text-align: justify;">
    Every crash record in our dataset includes an operator, which could be a military body, a commercial airline, or an individual private pilot. We grouped these into four categories: </p>
<ul>
    <li>Civilian/Commercial </li>
    <li>Military </li>
    <li>Private </li>
    <li>Other/Unknown </li>
  </ul>

<p style="text-align: justify;">
Using this classification, we created a series of interactive line charts showing how crash counts per year differ by operator category. 
<br>
<br>

[Interactive Bokeh Line Chart: Accidents per Year by Operator Type] 
<br>
<br>

Military aviation historically reports the highest number of accidents, especially before the 1990s. Civilian aviation, while more prominent today, shows a steady decrease in major accidents since the early 2000s. </p>
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

 </p>

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
