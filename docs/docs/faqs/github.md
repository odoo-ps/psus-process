---
layout: post
title:  "Github"
permalink: /faqs/github/
parent: FAQs
categories: jekyll update
---


[How to transfer branch to customer (SaaS]() <br />
[How to transfer repo to customer (SH)]() <br />

1. Create a copy of ps-custom in folder ps-custom_bis

```
git clone git@github.com:odoo/ps-custom.git ps-custom_bis
```

2. Go into this folder

```
cd ps-custom_bis
```

3. Checkout the branch you want to copy

```
git checkout <branch_to_copy>
```
4. Change the remote url to your new repo

```
git remote set-url origin git@github.com:odoo-ps/psus-custom.git
```
5. Push the branch on your new repo

```
git push
```
You can also change the name of the branch transferred

6. Checkout the branch transferred

```
git checkout <branch_transferred>
```

7. Change name locally to for example 12.0-module_saas_backup

```
git branch -m <new_name>
```

8. Set new upstream

```
git push origin -u <new_name>
```

9. Delete old name remote branch:

```
git push origin --delete <old_name>
```
After that you can delete the folder ps-custom_bis from your computer. You now have previous dev with history on the new repository.