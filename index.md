---
layout: default
---
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>ICS files for SIFF's cinemas</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.8/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-sRIl4kxILFvY47J16cr9ZwB07vP4J8+LH7qKQnuqkuIAvNWLzeN8tE5YBujZqJLB" crossorigin="anonymous">
  </head>

<body>

<a href="{{ site.github.repository_url }}"><img decoding="async" loading="lazy" width="149" height="149" src="https://github.blog/wp-content/uploads/2008/12/forkme_right_darkblue_121621.png?resize=149%2C149" class="attachment-full size-full" alt="Fork me on GitHub" data-recalc-dims="1" style="position: absolute; top: 0; right: 0; border: 0;"></a>

<div class="container my-5">

<a href="https://www.siff.net/">
    <img src="assets/logo.png?{{ site.github.build_revision }}" height="100" class="mb-5">
</a>

<h1>ICS files for SIFF venues</h1>

<p>
    This website provides `.ics` files for upcoming <a href="https://www.siff.net/">SIFF</a>
    movies so that you can see the schedule in your regular calendar with your other
    events. This makes it easier to see whether you are free and/or can arrange
    double bills etc.
</p>

<p>
    The end times of the movies are automatically calculated based on the
    duration of the movie, but padding is added as well to accommodate
    trailers. Each entry's 'Description' field contains the synopsis of the
    film.
</p>

<p>
    In addition, during the SIFF festival, this description field also includes
    the other times and locations a movie might be playing. The padding is
    adjusted as well.
</p>


<p class="text-center">
  <big><big><strong><a class="btn btn-primary btn-lg" href="ics/all.ics?{{ site.github.build_revision }}">Right-click me and select <em>Copy link address</em></a></strong></big></big>
</p>

<hr class="m-5">

<p class="mt-4">Individual ICS files for each venue:</p>

<ul class="list-unstyled">
{% for venue in site.data.venues %}
<li>
    <a class="btn mt-1 btn-secondary" href="ics/{{ venue.VenueSlug }}.ics?{{ site.github.build_revision }}">{{ venue["VenueNameOrig"] }}</a>
</li>
{% endfor %}
</ul>

<hr class="m-5">

<h2 class="mt-5 mb-3">Instructions</h2>

<p>
  <img src="assets/screenshot.png?{{ site.github.build_revision }}">
</p>

<p>
  Copy-paste an ICS link from above, and import using <em>From URL</em> within Google Calendar.
</p>

<p class="mt-5"><a href="{{ site.github.repository_url }}/commit/{{ site.github.build_revision }}">Last update</a></p>

</div>

</body>
