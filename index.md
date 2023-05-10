---
layout: default
---

<a href="{{ site.github.repository_url }}"><img decoding="async" loading="lazy" width="149" height="149" src="https://github.blog/wp-content/uploads/2008/12/forkme_right_darkblue_121621.png?resize=149%2C149" class="attachment-full size-full" alt="Fork me on GitHub" data-recalc-dims="1" style="position: absolute; top: 0; right: 0; border: 0;"></a>

<a href="https://www.siff.net/">
    <img src="assets/logo.png?{{ site.github.build_revision }}" height="100">
</a>

<body>

<h1>ICS files for SIFF 2023</h1>

<p>
  <big><strong><a href="ics/all.ics?{{ site.github.build_revision }}">All events</a></strong> (.ics)</big>
</p>

<p>Venues:</p>

<ul>
{% for venue in site.data.venues %}
<li>
    {{ venue["VenueName"] }} (<a href="ics/{{ venue.VenueSlug }}.ics?{{ site.github.build_revision }}">ICS</a>,
        <a href="https://larrybolt.github.io/online-ics-feed-viewer/#feed={{ site.url|url_encode }}{{ site.baseurl|url_encode }}/ics/{{ venue.VenueSlug }}.ics%3F{{ site.github.build_revision }}&cors=false&title={{ venue.VenueName|url_encode }}">View</a>, <a href="https://www.google.co.uk/maps/search/{{ venue.VenueName|url_encode }}%20{{ venue.VenueAddress1|url_encode }}">Google Maps</a>)
</li>
{% endfor %}
</ul>

<h2>Instructions</h2>

<p>
  <img src="assets/screenshot.png?{{ site.github.build_revision }}">
</p>

<p>
  Copy-paste an ICS link from above, and import using <em>From URL</em> within Google Calendar.
</p>

<p><a href="{{ site.github.repository_url }}/commit/{{ site.github.build_revision }}">Last update</a></p>
