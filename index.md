<div>
    <style>
        h3 {text-align:center;}
        .plist
        {
            float:left;
            width:300px;
            height:280px;
            margin:5px;
        }
    </style>
    {% for category in site.categories %}
        <h3>{{ category[0] }}</h3>
        <hr>
        {% for post in category[1] %}
            <div class="plist">
                <img src="{{post.img}}"/>
                <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
        {% endfor %}
    {% endfor %}
</div>
