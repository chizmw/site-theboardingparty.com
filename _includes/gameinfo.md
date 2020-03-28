{%- assign bgggamename = include.bgggamename -%}
<span class="gameinfolinks">
{%- if include.bgggameid -%}
<span><a href="https://boardgamegeek.com/boardgame/{{ include.bgggameid| cgi_escape | escape }}"><span class="gamelinkdestination">Read more about</span> <span class="gametitle">{{include.bgggamename |default:'BoardGameGeek'}}</span> <span class="gamelinkdestination">on BoardGameGeek</span></a> <i class="fad fa-dice"></i></span>{: .text-right style="text-align: right; display: block;"}
{%- endif -%}
{%- if include.zatuproduct - %}
<span><a href="https://www.board-game.co.uk/product/{{include.zatuproduct| cgi_escape | escape }}/"><span class="gamelinkdestination">Purchase</span> <span class="gametitle">{{include.bgggamename}}</span> <span class="gamelinkdestination">from Zatu</span></a> <i class="fas fa-shopping-cart"></i></span>{: .text-right style="text-align: right; display: block;"}
{%- endif -%}
{%- if include.amazonid -%}
<span><a href="https://smile.amazon.co.uk/dp/{{include.amazonid| cgi_escape | escape }}/"><span class="gamelinkdestination">Purchase</span> <span class="gametitle">{{include.bgggamename}}</span> <span class="gamelinkdestination">from Amazon UK</span></a> <i class="fab fa-amazon"></i></span>{: .text-right style="text-align: right; display: block;"}
{%- endif -%}
{%- if include.bgpricesid -%}
<span><a href="https://boardgameprices.co.uk/item/show/{{include.bgpricesid| cgi_escape | escape }}/"><span class="gamelinkdestination">Find the best prices for</span> <span class="gametitle">{{include.bgggamename}}</span> <span class="gamelinkdestination">on BoardGamePrices</span></a> <i class="fas fa-search-dollar"></i></span>{: .text-right style="text-align: right; display: block;"}
{%- endif -%}
</span>
