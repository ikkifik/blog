---
layout: default
title: Utas
---
<h1 style="text-align: center; font-size: 40pt;">@</h1>

{% for thread in site.data.threads.threads limit:5%}
  <li class="thread-item">
    <p><strong>[{{ thread.date | date: "%b %d, %Y" }}]</strong> {{thread.caption}}</p>
    
    {% if thread.media %}
    <div class="thread-media">
      <iframe 
        src="https://www.youtube.com/embed/{{ thread.media }}" 
        frameborder="0" 
        referrerpolicy="no-referrer-when-downgrade">
      </iframe>
    </div>  
    {% endif %}
  </li>
{% endfor %}

<p class="thread-footer">
  This page is a clone-like Threads by Meta for expressing my personal feelings that I do not feel like to share on the official one. I do have the official Threads account, you can follow me on <a href="https://www.threads.net/@__zuhdifikri" target="_blank">@Threads</a>.
</p>