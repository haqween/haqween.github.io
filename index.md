<div>
    <style>
        h3 {text-align:center;}
        .plist
        {
            float:left;
            width:110px;
            height:90px;
            margin:5px;
        }
    </style>
    {% for category in site.categories %}
        <h3>{{ category[0] }}</h3>
        <hr>
        {% for post in category[1] %}
            <div class="plist">
                <img src="{{post.img}}" width="304" height="228"/>
                <a href="{{ post.url }}">{{ post.title }}</a>
            </div>
        {% endfor %}
    {% endfor %}
</div>
