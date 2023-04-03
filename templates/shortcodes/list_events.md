{% set meetups = load_data(path="events.toml") %}

{% if meetups[group] %}
## {{ group | capitalize }}

{% for item in meetups[group] %}
### {{ item.title }}

{% if item.url %}**Link:** [Meetup.com]({{ item.url }}){% endif %}  
**Date:** {% if item.date %}<time datetime="{{ item.date }}">{{ item.date | date(format="%A, %e %B %Y", timezone="Europe/Berlin") }}</time>  {% else %}(No date found)  {% endif %}
**Venue:** {% if item.venue %}{{ item.venue }} – {% endif %}{% if item.address %}{{ item.address }}   {% else %}(No venue)  {% endif %}
{% if item.content -%}**Description:**<blockquote>{{ item.content | safe }}</blockquote>{% endif %}

{% endfor %}
{% endif %}
