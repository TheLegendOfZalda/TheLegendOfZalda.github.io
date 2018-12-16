---
layout: page
title: Secrets inside Clinton's email
bigimg: profile.png
---
> By Junze Li, Yusi Zou, Zhantao Deng

{% include_relative _includes/styles.html %}
{% include_relative _includes/scripts.html %}


# **Background**
<div align="justify">
<p>In 2015, Hillary Clinton has been embroiled in controversy over the use of personal email accounts on non-government servers during her time as the United States Secretary of State. Over 2000 confidential emails were leaked, some of them are even classified as “Top Secret”. </p>

<p>We will look at the politic, security and economic aspects through the 7945 leaked emails redacted and published by the State Department and cleaned by <a href="https://www.kaggle.com/kaggle/hillary-clinton-emails">Kaggle</a>. We will also analyze the personal social network of Hillary Clinton and the top topics they discussed.</p>

<p>As a superpower, the United States has a great impact on the world’s stability, and their position and attitude will strongly influence the international affairs. We want to figure out the countries mainly mentioned, the problems concerned and conclude the impact they made on the international affairs throughout the analysis of these emails.</p>
</div>
&nbsp;

---
&nbsp;

# **Who is she talking to?**
<div align="justify"><p>
	Let's first have a look at to whom does Hillary communicate most in both directions.
</p></div>

<div align="center">
	<font size="+1">Receivers of emails sent by Hillary</font>
</div>

<div id="pie3"></div>
{% include_relative _includes/pie3.html %}

<div align="justify">
<p>We can see that Hillary Clinton writes mostly to these 5 people: they receive 81% of all emails that Hillary writes! </p>
<p>Is there a similar case for the inverse direction of the communication?🤔 </p>
</div>

&nbsp;

<div align="center">
	<font size="+1">Sender of emails received by Hillary</font>
</div>

<div id="pie4"></div>
{% include_relative _includes/pie4.html %}

<div align="justify">
Again, 5 people write 83% of emails that are written to Hillary! However, the important people change. We highlight those people and have a glance at their position.
</div>

&nbsp;

<button class="button" onclick="changeContactPeople('Huma Abedin')">Huma Abedin</button>
<button class="button" onclick="changeContactPeople('Cheryl Mills')">Cheryl Mills</button>
<button class="button" onclick="changeContactPeople('Jacob Jeremiah Sullivan')">Jacob Jeremiah Sullivan</button>
<button class="button" onclick="changeContactPeople('Sidney Blumenthal')">Sidney Blumenthal</button>

<p id="description">
<b>Huma Abedin</b> : the most frequent sender.<br><br>  -<i><b>Vice chair of Hillary Clinton's 2016 campaign</b> for President of the United States.</i><br><br>  -<i><b>Deputy chief of staff to Clinton</b>, who was U.S. Secretary of State from 2009 to 2013.</i><br><br>  -<i><b>Traveling chief of staff and former assistant for Clinton</b> during Clinton's campaign for the Democratic nomination in the 2008 presidential election.</i><br><br><i>An interesting observation: She receives the most emails FROM Hillary, but is only the 8-th sender of emails TO Hillary. We guess that she excutes more Hillary's order than make reports.</i><br><br>She is clearly the right-hand woman of Hillary Clinton.
</p>

<div align="center">
	<font size="+1">____________________</font>
</div>

<div align="justify">
<p>These are people with whom Hillary communicate most frequently, and they are clearly politicians, collegues of Hillary Clinton. She definitely use her personal email accounts on non-government servers and send professional emails to her collegues during her time as the United States Secretary of State, which is a severe threat for the national security.</p>

<p>According to the FBI examination, <i>"over 100 emails containing classified information, including 65 emails deemed "Secret" and 22 deemed "Top Secret", none with classification markings. An additional 2,093 emails not marked classified were retroactively classified by the State Department."</i>(wikipedia). It is almost unimaginable how come a politician at her position can be that inprudent.😨</p>
</div>

<div align="center">
	<font size="+1">____________________</font>
</div>
&nbsp;

### Some interesting observations

<font size="+1"><b>Emails from anonymous senders are mostly partially released</b></font>

<div align="justify">
The data set provides us informtion about whether the email is fully or partially released by the States Department. We use this information to observe whether this is related to the anonymity of senders. 
</div>

{% include_relative _includes/double_pie.html %}

<div align="justify">
<p>The anonymous emails sent to Hillary are possibly more confidential, that the sender is erased by the State Department before release. Almost all of them are released partially.</p>
</div>
&nbsp;

<font size="+1"><b>Hillary as sender VS Hillary as receiver</b></font>

<div id="pie5"></div>
{% include_relative _includes/pie5.html %}

<div align="justify">Among all emails released by the State Department, 25.08% are sent by Hillary Clinton and 68.94% are received by Hillary.</div>

&nbsp;

---
&nbsp;

# **Which country is focused?** 

<iframe src="map_borders.html" width="100%" height="400">Your browser does not support iframes.</iframe>

{% include_relative _includes/bar_plot_top20_occurence.html %}

It is obvious that asian countries and middle east countries are the most frequently mentioned countries in Hillary's emails. There are also some european countries and central america countries often appear in the emails, such as the United Kingdom and Haiti.  

Middle east countries like Pakistan, Afghanistan, Oman, Iran, Iraq and Israel are the top 6 countries mentioned in the emails.  

**Is there some relation with the events happening at that moment?**  

<video width="720" height="480" autoplay muted loop>
  <source src="country-occ.mp4" type="video/mp4">
  <p>Your browser does not support the video element.</p>
</video>


Let's have a look at the timing of mentioning those countries.
>根据时间和事件分别分析重点国家，如海地利比亚之类的，多几个国家，可以参考我们的model

&nbsp;

---
&nbsp;

# **What does she think about these countries?**
Hillary was the secretary of state and responsible for diplomacy of US in the period from 2008 to 2013. Therefore, from her emails, we can find out the attitude of US in diplomatic relations with other countries.

{% include_relative _includes/positive_sentiment.html %}





&nbsp;

&nbsp;

The Hilary's emails are within the period from 2008 to 2013, so we will associate US's policy and international events to the sentiments of Hilary's emails. We highlight some countries and regions here:

**China**:
  Obama was friendly with China during his presidency, and as a result, the bilateral relationship between China and US, two superpower in the world, maintains more or less stable in this period. For example, at the end of 2014, the US government carried out for the first time a 10-year visa policy to promote communication between the two countries. Meanwhile, after the 2008 international financial crisis, US was strongly influenced and wanted to recover it by strengthening cooperation in economics with China.

**India**:
India, as the largest democracy country in population, has always maintained a closed bilateral relations with US and has widely communication and cooperation in economics and technology with US.

**Oman**:
Oman is a Middle East country with abundant oil reserve and the fortress country of the Strait of Hormuz, which attracts the attention of US government. And US and Oman launched negotiations on a Free Trade Agreement that were successfully concluded in October 2005. So the bilateral relation is positive and stable.   

**Haiti**:
Haiti suffered a serious earthquake in January 2010. President Obama announced a 100m$ US aid package to help Haiti. We think that the emails mentioning Haiti are about supporting Haiti.

**Russia**:
The Crimean Crisis happened in 2014, and the tension was only after the crisis. Before the crisis Russia and US had kept cooperation.

**Japan, Brasil, Hongkong, ... :**
Those are countries or region which are important economies and have no big conflit with US. So we think that emails mentioning these countries talk especially about cooperation.

**Qatar, Turkey, ... :**
These Middle-east countries had no economic or political conflit with US at that period and US do need cooperation with countries with abundant oil reserve and alliance countries in the Middle-east area.



After analysis about the bilateral relations with some typical countries or region, we find that the positive sentiment countries have the following properties:
- Long-term friendly country by historical reasons
- Important fortress country in channel or other transportation line
- Country with abundant oil reserve
- Economically cooperative country without conflict of interest

&nbsp;

{% include_relative _includes/negative_sentiment.html %}

&nbsp;

Same as for the positive sentiment countries, we highlight the following countries to analyze:

**North Korea**: North Korea conducted two nuclear explosion tests during this period, respectively in May 2009 for the first time ever in the history and February 2013 for the second time. The US government claimed that the test will affect international security and strongly opposed this kind of test. So sentiment in emails to North Korea is negative in this period of time. 

**Libya**: In 2012, when Benghazi, the base camp of the opposition force, is almost occupied by the Gaddafi government, the [Benghazi attack](https://en.wikipedia.org/wiki/2012_Benghazi_attack) took place and the US ambassador to Libya was killed, This caused a serious consequence: the United Nations Security Council passed a resolution and US, together with United Kingdom and France, bombed Libya by air force. Hillary, as the Secretary of State during this period, mostly took charge of US diplomacy, so her emails mentioning Libya must had been with negative sentiments, as it was a serious international incident.

**Germany, United Kingdom, France ... :** These are major countries in North Atlantic Treaty Organization (NATO) which participated the action to bomb Libya. The cooperation at this level certainly talked about negative subject as NATO is a military alliance.

After analysis about the bilateral relations with some typical countries, we find that countries with which Hillary had a negative sentiment all have one of the following properties:
- Country in NATO taking the same position with US
- Country with an unstable government or with an difficult political situation

{% include_relative _includes/Libya.html %}

&nbsp;

---
&nbsp;

# **What are the main topics?**
>wordcloud  
>分析一通这些词  

&nbsp;

> TF IDF matrix  
> 分析一通，按国家

&nbsp;

---
&nbsp;

# **Conclusion**
> you know...