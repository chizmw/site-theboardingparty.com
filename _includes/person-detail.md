{% assign person = site.data.hosts-map |where:"hostid", page.hostid |first %}

{% if person.bgg and person.bgg.username%}
## BoardGameGeek

* [<i class="fas fa-user-circle"></i> Profile <small><i class="fad fa-external-link"></i></small>](https://boardgamegeek.com/user/{{ person.bgg.username }})
* [<i class="fas fa-inventory"></i> Base Games <small><i class="fad fa-external-link"></i></small>](https://boardgamegeek.com/collection/user/{{ person.bgg.username }}?gallery=large&rankobjecttype=subtype&rankobjectid=1&excludesubtype=boardgameexpansion&own=1&objecttype=thing&ff=1&subtype=boardgame)
* [<i class="fas fa-th-list"></i> Plays <small><i class="fad fa-external-link"></i></small>](https://boardgamegeek.com/plays/bydate/user/{{ person.bgg.username }}/subtype/boardgame)
{% endif %}
