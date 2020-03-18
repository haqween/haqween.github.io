<div>
    <style>
        h3 {text-align:center;}
    </style>
    {% for category in site.categories %}
    <div>
        <h3>{{ category[0] }}</h3>
        <hr>
        <table> <tr>
        {% for post in category[1] %}
            <td>
                <img src="{{post.img}}" width="200" height="120"/>
                <br/>
                <a href="{{ post.url }}">{{ post.title }}</a>
            </td>
        {% endfor %}
        </tr> </table>
    </div>
    {% endfor %}
</div>
