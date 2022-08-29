---
layout: post
title:  "Transfer Branches"
# permalink: /branchtransfer/
date:   2022-08-29 10:19:51 -0700
categories: jekyll update
parent: Process

---

1. Create a copy of ps-custom in folder ps-custom_bis

{% highlight ruby %}
git clone git@github.com:odoo/ps-custom.git ps-custom_bis
{% endhighlight %}

2. Go into this folder

{% highlight ruby %}
cd ps-custom_bis
{% endhighlight %}

3. Checkout the branch you want to copy
{% highlight ruby %}
git checkout <branch_to_copy>
{% endhighlight %}

4. Change the remote url to your new repo

{% highlight ruby %}
git remote set-url origin git@github.com:odoo-ps/psus-custom.git
{% endhighlight %}

5. Push the branch on your new repo
{% highlight ruby %}
git push
{% endhighlight %}
You can also change the name of the branch transferred

6. Checkout the branch transferred

{% highlight ruby %}
git checkout <branch_transferred>
{% endhighlight %}

7. Change name locally to for example 12.0-module_saas_backup
{% highlight ruby %}
git branch -m <new_name>
{% endhighlight %}

8. Set new upstream
{% highlight ruby %}
git push origin -u <new_name>
{% endhighlight %}

9. Delete old name remote branch:
{% highlight ruby %}
git push origin --delete <old_name>
{% endhighlight %}

After that you can delete the folder ps-custom_bis from your computer. You now have previous dev with history on the new repository.