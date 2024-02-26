---
title: "FB Automate Group Leave"
categories: "Tools"
---

I create this project in order to my "Re:L" project, which I use to trying re-arrange my life. One of the ways to do that is to "clean up" my social media account so I can start again without actually restarting from scratch.  

FB Automate Group Leave is a program to automate leaving joined group, it's requires your email and password account to login into your FB account that you want to leave group. This program is safe as long as you don't share your FB account to anyone.  

----

## How to install  

1. Clone the repository  
{% highlight bash %}
git clone https://github.com/ikkifik/fb-automate-group-leave.git
{% endhighlight %}

2. Create and use virtual environment  
{% highlight bash %}
python3 -m venv fbvenv
source fbvenv/bin/activate
{% endhighlight %}

3. Get into directory  
{% highlight bash %}
cd fb-automate-group-leave
{% endhighlight %}

4. Install required package  
{% highlight bash %}
pip install -r requirements.txt
{% endhighlight %}

5. Run the program!
{% highlight bash %}
python leave_group.py \ 
--email <your_email_account> \ 
--pwd <your_password_account>
{% endhighlight %}

Here's how it's look:

![FB Automate Group Leave Preview](/assets/images/project-image/fb-automate-group-leave.png)
