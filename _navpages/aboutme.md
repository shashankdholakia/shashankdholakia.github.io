---
title: About Me
layout: page
idname: aboutme
---
I'm Shashank! I'm a first year PhD student in astrophysics at University of Queensland in Brisbane, Australia. I also enjoy [photography](https://www.brahmand.me) and play badminton. <br>

Wrong guy? You might be looking for [him](https://shishirdholakia.github.io)

___

<h2 style="margin-bottom:1em"> <b> My life and education </b> </h2>

<section style="margin-left:1.0em">
<div id="timeline_container">
	<div id="timeline"></div>
	<div id="events_container">

		{% assign sortedEvents = site.timeline | sort: 'date' | reverse %}
		{% assign timelineYear = 3000 %}
		<!-- One individual Event-->
			{% for event in sortedEvents %}
			{% if event.year < timelineYear %}
				<div class="year_marker">{{ event.year }}</div>
				{% assign timelineYear = event.year %}
			{% endif %}
			<div class="timeline_event">
				<div class="event_marker"></div>
				<div class="event_information">
					<h3 class="event_title"><b>{{ event.name }} </b></h3>
					<div class="icon solid fa-{{ event.icon_name }}" style="color:#3F51B5;">    {{ event.type }} </div>
					{{ event.content | markdownify }}
				</div>
			</div>
		{% endfor %}
		<!---->
			</div>
		</div>
</section>
