---
layout: post
title:  "Github"
permalink: /faqs/github/
parent: FAQs
categories: jekyll update
---


[How to transfer branch to customer (SaaS)]()  
[How to transfer repo to customer (SH)]()  

### Transfer branch from ps-custom to new psus-custom  
1. Create a copy of ps-custom in folder ps-custom_bis
```sh
git clone git@github.com:odoo/ps-custom.git ps-custom_bis 
```
2. Go into this folder
```sh
cd ps-custom_bis
```
3. Checkout the branch you want to copy
```sh
git checkout <branch_to_copy>
```
4. Change the remote url to your new repo
```sh
git remote set-url origin git@github.com:odoo-ps/<new_repo>.git
```
5. Push the branch on your new repo
```sh
git push
```
 You can also change the name of the branch transferred
 
6. Checkout the branch transferred
```sh
git checkout <branch_transferred>
```
7. Change name locally to for example 12.0-module_saas_backup
```sh
git branch -m <new_name>
```
8. Set new upstream
```sh
git push origin -u <new_name>
```
9. Delete old name remote branch:
```sh
git push origin --delete <old_name>
```

After that you can delete the folder ps-custom_bis from your computer.  
You now have previous dev with historic on the new repository. 