---
layout: page
title: Secrets inside Clinton's emails
---

{% include_relative _includes/styles.html %}
{% include_relative _includes/scripts.html %}

<!--COVER-->
<img src="/img/cover.jpg" class="img-centered" style="width:100%; height=100%;">

> By Junze Li, Yusi Zou, Zhantao Deng

<!--CHAPTER: BACKGROUD-->
<div align="center">
<font size="+1"><h1><b>Background</b></h1></font>
</div>

<div align="justify">
<p>In 2015, Hillary Clinton was embroiled in controversy over the use of personal email accounts on non-government servers during her time as the United States Secretary of State. Over 2000 confidential emails were leaked, some of them are even classified as “Top Secret”. </p>

<p>We will look at the politic, security and economic aspects through the 7945 leaked emails redacted and published by the State Department and cleaned by <a href="https://www.kaggle.com/kaggle/hillary-clinton-emails">Kaggle</a>. We will also analyze the personal social network of Hillary Clinton and the top topics they discussed.</p>

<p>As a superpower, the United States has a great impact on the world’s stability, and their position and attitude will strongly influence the international affairs. We want to figure out the countries mainly mentioned, the problems concerned and conclude the impact they made on the international affairs throughout the analysis of these emails.</p>
</div>
&nbsp;

---
<!--CHAPTER: NETWORK-->
&nbsp;

<div align="center">
<font size="+1"><h1><b>Who is she talking to?</b></h1></font>
</div>


<div align="justify"><p>
	Let's first have a look at to whom does Hillary communicate most in both directions.
</p></div>

<div align="center">
	<font size="+1">Receivers of emails sent by Hillary</font>
</div>

<!--PIE RECEIVERS-->
<div id="pie3"></div>
{% include_relative _includes/pie3.html %}

<div align="justify">
<p>We can see that Hillary Clinton writes mostly to these 5 people: they receive 81% of all emails that Hillary writes! </p>
<p>Is there a similar case for the inverse direction of the communication?</p>
</div>


<div align="center">
	<font size="+1">Senders of emails received by Hillary</font>
</div>

<!--PIE SENDERS-->
<div id="pie4"></div>
{% include_relative _includes/pie4.html %}

<div align="justify">
Again, 5 people write 83% of emails that are written to Hillary! However, the important people change. We highlight those people and have a glance at their position.
</div>

&nbsp;

<!--BUTTONS-->

<font size="-1"><i>Click on their photos to see their political position. </i></font><br>
<button class="button" onclick="changeContactPeople('Huma Abedin')"><img src="/img/huma.jpg" style="width:60%; height=60%;"></button>
<button class="button" onclick="changeContactPeople('Cheryl Mills')"><img src="/img/cheryl.jpg" style="width:60%; height=60%;"></button>
<button class="button" onclick="changeContactPeople('Jacob Jeremiah Sullivan')"><img src="/img/jake.jpg" style="width:60%; height=60%;"></button>
<button class="button" onclick="changeContactPeople('Sidney Blumenthal')"><img src="/img/sidney.jpg" style="width:60%; height=60%;"></button>

<p id="description">
<b>Huma Abedin</b> : the most frequent sender.<br><br>   -<i><b>Vice chair of Hillary Clinton's 2016 campaign</b> for President of the United States.</i><br>  -<i><b>Deputy chief of staff to Clinton</b>, who was U.S. Secretary of State from 2009 to 2013.</i><br>  -<i><b>Traveling chief of staff and former assistant for Clinton</b> during Clinton's campaign for the Democratic nomination in the 2008 presidential election.</i><br><br><i>An interesting observation: She receives the most emails FROM Hillary, but is only the 8-th sender of emails TO Hillary. We guess that she excutes more Hillary's order than make reports.</i><br>She is clearly the right-hand woman of Hillary Clinton.
</p>

<div align="center">
	<font size="+1">____________________</font>
</div>

<div align="justify">
<p>These are people with whom Hillary communicate most frequently, and they are clearly politicians, colleagues of Hillary Clinton. She definitely use her personal email accounts on non-government servers and send professional emails to her colleagues during her time as the United States Secretary of State, which is a severe threat for the national security.</p>

<p>According to the FBI examination, <i>"over 100 emails containing classified information, including 65 emails deemed "Secret" and 22 deemed "Top Secret", none with classification markings. An additional 2,093 emails not marked classified were retroactively classified by the State Department."</i>(wikipedia). That's shocking.</p>
</div>

<div align="center">
	<font size="+1">____________________</font>
</div>
&nbsp;

<!--Some interesting observations-->

<font size="+1"><b>Emails from anonymous senders are mostly partially released</b></font>

<div align="justify">
The data set provides us informtion about whether the email is fully or partially released by the States Department. We use this information to observe whether this is related to the anonymity of senders. 
</div>

<!--PIE ANONYMITY-->
{% include_relative _includes/double_pie.html %}

<div align="justify">
<p>The anonymous emails sent to Hillary are possibly more confidential, that the sender is erased by the State Department before release. Almost all of them are released partially.</p>
</div>
&nbsp;

<font size="+1"><b>Hillary as sender VS Hillary as receiver</b></font>
&nbsp;
<!--PIE SENDER/RECEIVER-->
<div id="pie5"></div>
{% include_relative _includes/pie5.html %}

<div align="justify">Among all emails released by the State Department, 25.08% are sent by Hillary Clinton and 68.94% are received by Hillary.</div>

&nbsp;

---
<!--CHAPTER: OCCURRENCE-->
&nbsp;

<div align="center">
<font size="+1"><h1><b>Which countries are discussed?</b></h1></font>
</div>

Let's have a general idea about what countries are mentioned mostly.
<!--MAP-->
<iframe src="map_borders.html" width="100%" height="400">Your browser does not support iframes.</iframe>
<img src="/img/colorbar.jpeg" class="img-centered" style="width:50%; height=50%;">

<!--OCCURENCE BAR-->
From there we extract the top 20 countries that are frequently discussed in the emails.
{% include_relative _includes/bar_plot_top20_occurence.html %}

And the strategic focus of Hillary Clinton, with respect to the total number of emails that countries in these regions/continents are mentioned:

<!--RADAR-->
<img src="/img/radarplot.png" class="img-centered" style="width:70%; height=70%;">

<div align="justify">
<p>It is obvious that the Middle East is the main focus of U.S. at that time. Most of the top 20 frenquently discussed countries are from this region. However, Haiti appeares surprisingly more than 400 times in Hillary's emails but it is not really a "big" country. This is possibly because the 2009 Haiti earthquake.</p>
<p>There are also some asian, european and central america countries often appear in the emails, such as the United Kingdom, China and Haiti. Later we will analyse them in detail.</p>
</div>

&nbsp;

---
<!--CHAPTER: TIME SERIES-->
&nbsp; 

<div align="center">
<font size="+1"><h1><b>Are the emails related to the international events?</b></h1></font>
</div>


<div align="justify">
Let's have a look at what events cause discussions of these country between Hillary and her colleagues. Here's a visualization of the evolution of the times that countries are mentioned in the emails, per month.
</div>

<!-- VIDEO-->
<video width="720" height="480" autoplay muted loop>
  <source src="country-occ.mp4" type="video/mp4">
  <p>Your browser does not support the video element.</p>
</video>

<div align="justify">
Let's first figure out the keywords in her emails. 

<!-- WORDCLOUD-->
<img src="/img/wordcloud.png" class="img-centered" style="width:80%; height=80%;">

Here we also construct a <a href="https://en.wikipedia.org/wiki/Tf%E2%80%93idf">TF-IDF</a> matrix indicating the importance of words by country.
</div>

<!--TF-IDF-->
{% include_relative _includes/TF-IDF.html %}
&nbsp; 

<div align="justify">
<p>This gives us an idea about the events related to each country. Is it related to what they discussed in the emails?</p>

<p>We can figure it out by grouping occurrences by month and draw several line charts. </p>
</div>

<!--TOP 3, MIDDLE EAST-->
{% include_relative _includes/Libya.html %}
<div align="justify">
<font size="+1"><span style="color:#537fc6;"><b>Libya</b></span>: <span style="background-color:#fffdc4">Benghazi Attack</span> <i>September 2012</i></font>
<p>At 9:40 p.m., September 11, 2012, members of Ansar al-Sharia attacked the American diplomatic compound in Benghazi resulting in the deaths of U.S. Ambassador to Libya J. Christopher Stevens and U.S. Foreign Service Information Management Officer Sean Smith.</p>

<font size="+1"><span style="color:#f76767;"><b>Afghanistan</b></span>: <span style="background-color:#fffdc4">Kunduz airstrike</span> <i>September 2009</i></font>
<p>On Friday 4 September 2009 at roughly 2:30 am, as responding to a call by German forces, an American F-15E fighter jet struck two fuel tankers captured by Taliban insurgents in Kunduz province in northern Afghanistan, killing over 90 civilians in the attack. Many countries criticized the airstrike.</p>

<font size="+1"><span style="color:#45d87b;"><b>Israel</b></span>: <span style="background-color:#fffdc4">Israeli–Palestinian peace talks</span> <i>September 2010</i></font>
<p>Direct negotiations between Israel and the Palestinian National Authority took place in September 2010 as part of the peace process, between United States President Barack Obama, Israeli Prime Minister Benjamin Netanyahu, and Palestinian Authority Chairman Mahmoud Abbas.</p>
</div>

<div align="center">
	<font size="+1">____________________</font>
</div>
&nbsp;

<!--EU THREE-->
{% include_relative _includes/France.html %}
<div align="justify">
<font size="+1"><b>EU three, P5+1</b>: <span style="background-color:#fffdc4">Iran nuclear program</span></font><br>

<font size="+1"><i>September 2009</i></font><br>
<p>On 21 September 2009, Iran informed the IAEA that it was constructing a second enrichment facility. The following day IAEA Director General ElBaradei informed the United States, and two days later (24 September) the United States, United Kingdom and France briefed the IAEA on an enrichment facility under construction at an underground location at Fordu, 42 kilometres north of Qom. </p>
<font size="+1"><i>November 2009</i></font><br>
<p>In November 2009, the IAEA's 35-nation Board of Governors overwhelmingly backed a demand that Iran immediately stop building its newly revealed nuclear facility and freeze uranium enrichment.</p>
</div>

<div align="center">
	<font size="+1">____________________</font>
</div>
&nbsp;

<!--BRAZIL CHINA-->
{% include_relative _includes/Brazil.html %}
<div align="justify">
<font size="+1"><span style="color:#537fc6;"><b>Brazil</b></span>: <span style="background-color:#fffdc4">Abduction of children</span> <i>December 2009</i></font><br>
<p>The issue of the abduction of children from the United States to Brazil has been raised by Obama, Secretary of State Hillary Clinton, the United States House of Representatives and other U.S. officials and major media.</p>

<font size="+1"><span style="color:#e2a146;"><b>China</b></span>: <br>
<span style="background-color:#fffdc4">2009 Obama visit to China</span> <i>December 2009</i></font><br>
<p>US President Barack Obama visited China on November 15–18, 2009 to discuss economic worries, concerns over nuclear weapon proliferation, and the need for action against climate change.</p>
<font size="+1"><span style="background-color:#fffdc4">Approval of Taiwan Arms Sales</span> <i>January 2010</i></font><br>
<p>The Obama administration approved an arms sales package to Taiwan worth more than $6 billion, a move that enraged China.</p>
</div>


<div align="center">
	<font size="+1">____________________</font>
</div>
&nbsp;

<div align="justify">
As a superpower in the world, U.S. is a very important actor in international cooperations, competitions and military operations. So, there is a strong connection between international events and Hillary's emails. From above figures we can observe that, every event is followed by a peak of occurrence, which means that many Hillary's emails contain those countries involved in the event and possibly show the attitute of U.S govenment toward the event. Therefore, once these emails leaked to hostile countries, there could be serious threats to U.S. and its allies.
</div>
&nbsp;

---
&nbsp;

<!--CHAPTER: SENTIMENT ANALYSIS-->
<div align="center">
<font size="+1"><h1><b>What does she think about these countries?</b></h1></font>
</div>

<div align="justify">
<p>Hillary was the secretary of state and responsible for diplomacy of US in the period from 2008 to 2013. Therefore, from her emails, we can find out the attitude of US in diplomatic relations with other countries. </p>

<!--POSITIVE SENTIMENTS-->
<p>Let's first look at countries with which she presents a <span style="color:#c657a7;"><b>positive tone</b></span> in her emails.</p>
</div>

{% include_relative _includes/positive_sentiment.html %}

&nbsp;

<div align="justify">
<p>The Hilary's emails are within the period from 2008 to 2013, so we will associate US's policy and international events to the sentiments of Hilary's emails. We highlight some countries and regions here:</p>

<p><b>China</b>:
Obama was friendly with China during his presidency, and as a result, the bilateral relationship between China and US, two superpower in the world, maintains more or less stable in this period. For example, at the end of 2014, the US government carried out for the first time a 10-year visa policy to promote communication between the two countries. Meanwhile, after the 2008 international financial crisis, US was strongly influenced and wanted to recover it by strengthening cooperation in economics with China.</p>

<p><b>India</b>: 
India, as the largest democracy country in population, has always maintained a closed bilateral relations with US and has widely communication and cooperation in economics and technology with US.</p>

<p><b>Oman</b>:
Oman is a Middle East country with abundant oil reserve and the fortress country of the Strait of Hormuz, which attracts the attention of US government. And US and Oman launched negotiations on a Free Trade Agreement that were successfully concluded in October 2005. So the bilateral relation is positive and stable. </p>  

<p><b>Haiti</b>:
Haiti suffered a serious earthquake in January 2010. President Obama announced a 100m$ US aid package to help Haiti. We think that the emails mentioning Haiti are about supporting Haiti.</p>

<p><b>Russia</b>:
The Crimean Crisis happened in 2014, and the tension was only after the crisis. Before the crisis Russia and US had kept cooperation.</p>

<p><b>Japan, Brasil, Hongkong, ... </b>:
Those are countries or region which are important economies and have no big conflit with US. So we think that emails mentioning these countries talk especially about cooperation.</p>

<p><b>Qatar, Turkey, ... </b>:
These Middle-east countries had no economic or political conflit with US at that period and US do need cooperation with countries with abundant oil reserve and alliance countries in the Middle-east area.</p>
</div>

&nbsp;

After analysis about the bilateral relations with some typical countries or region, we find that the positive sentiment countries have the following properties:
- Long-term friendly country by historical reasons
- Important fortress country in channel or other transportation line
- Country with abundant oil reserve
- Economically cooperative country without conflict of interest

<div align="center">
	<font size="+1">____________________</font>
</div>
&nbsp;

<p>Now let's also look at countries with which she presents a <span style="color:#253366;"><b>negative tone</b></span> in her emails.</p>

{% include_relative _includes/negative_sentiment.html %}

&nbsp;

<!--NEGATIVE SENTIMENT-->
<div align="justify">
<p>Same as for the positive sentiment countries, we highlight the following countries to analyze:</p>

<p><b>North Korea</b>: North Korea conducted two nuclear explosion tests during this period, respectively in May 2009 for the first time ever in the history and February 2013 for the second time. The US government claimed that the test will affect international security and strongly opposed this kind of test. So sentiment in emails to North Korea is negative in this period of time. </p>

<p><b>Libya</b>: In 2012, when Benghazi, the base camp of the opposition force, is almost occupied by the Gaddafi government, the <a href="https://en.wikipedia.org/wiki/2012_Benghazi_attack">Benghazi attack</a> took place and the US ambassador to Libya was killed, This caused a serious consequence: the United Nations Security Council passed a resolution and US, together with United Kingdom and France, bombed Libya by air force. Hillary, as the Secretary of State during this period, mostly took charge of US diplomacy, so her emails mentioning Libya must had been with negative sentiments, as it was a serious international incident.</p>

<p><b>Germany, United Kingdom, France ... </b>: These are major countries in North Atlantic Treaty Organization (NATO) which participated the action to bomb Libya. The cooperation at this level certainly talked about negative subject as NATO is a military alliance.</p>
</div>

&nbsp;

After analysis about the bilateral relations with some typical countries, we find that countries with which Hillary had a negative sentiment all have one of the following properties:
- Country in NATO taking the same position with US
- Country with an unstable government or with an difficult political situation


&nbsp;

---
<!--CHAPTER: CONCLUSITON-->
&nbsp;

<div align="center">
<font size="+1"><h1><b>Conclusion</b></h1></font>
</div>

<div align="justify">
By explorating Hillary Clinton's emails, we conclude that: <br>

<ul>
- Hillary sends professional emails to her colleagues via her personal email account on non-government servers during her tenure as Secretary of State.<br>
- The keywords and topics in Hillary’s emails are associated with the international events.<br>
- The sentiment to other countries shown in her emails can reflect the national strategy of U.S. and may influence bilateral diplomatic relations. <br>
</ul>

<p>The above findings make us think that using personal emails for discussing international affaires may <b>cause severe consequences to the national security and diplomacy.</b></p>

<p>It is almost unimaginable how come a politician at her position can be that inprudent. Her "little" mistake may, in the worst case, <b>cause all people of her country in trouble</b>. The image, not only of Hillary's, but also of "American politicians" in general, is worsened from an outside point of view. </p>

<p><b>Surely that we hope to see a transparent world, but when something is related to confidential information concerning the national security, it should be prudently treated.</b></p>
</div>

&nbsp;

---
<!--CHAPTER: AUTHOR-->
&nbsp;

The research is made by the best team in the universe:   
<center><a href="https://github.com/TheLegendOfZalda"><b><font size="+2">TheLegendOfZalda</font></b></a></center>

<img src="/img/logo.png" class="img-centered" style="width:20%; height=20%;">

<font size="-2">The logo is inspired by the logo of <ins>Zelda: Breath of the Wild</ins>. This is a good game but has nothing to do with our project. It's just our team is named <b>Zalda</b>.</font>