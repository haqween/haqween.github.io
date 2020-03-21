<div>
    <style>
        h3 {text-align:center;}
        div.card{
            width: 200px;
            box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
            text-align: center;
            padding: 5px;
            margin: 0px 5px
        }
    </style>
    {% for category in site.categories %}
    <div>
        <h3>{{ category[0] }}</h3>
        <hr>
        <table> <tr>
        {% for post in category[1] %}
            <td>
            <div class="card" onclick="window.open('{{ post.url }}')">
                <img src="{{post.img}}" width="100%" height="120"/>
                <p class="container">{{ post.title }}</p>
            </div>
            </td>
        {% endfor %}
        </tr> </table>
    </div>
    {% endfor %}
</div>
