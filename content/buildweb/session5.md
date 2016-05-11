Title: Sesson 5
Date: 2016-05-05 16:00
Category: buildweb
Tags: session5
Type: section
Slug: session5

## Site Building

* Reading: "Updating and Security" below.

## Online Courses

## Web Fundamentals

* Reading: [What is Encryption?](https://ssd.eff.org/en/module/what-encryption)
* Reading: [Generating and remembering passwords](https://ssd.eff.org/en/module/creating-strong-passwords)
* Wordpress plugins

WordPress plugins are additional pieces of software you can add into your WordPress site.  Just like with themes, the developers of WordPress built in a catalog that lists thousands of free plugins to handle a whole range of different tasks and situations.  You can access this through your site's dashboard under "Plugins".  While all these pluins are free, just like with themes many will try and convince you to pay them for additional features and tools.  If you do need one of the paid features of a plugin, unless you have a reason you need to use that particular plugin, I would strongly advise returning to the plugin list to see if you can find a different one that can handle what you are trying to do for free. Plugins offer some great tools to make your site flexible and capable of doing whatever you might need but, because plugins are additional software you are installing, each one that you add makes your site a little more likely to break.  The best approach for plugins is to use as few as you can to accomplish what you need, choose plugins that are widely used and actively maintained where possible, and keep them updated along with the rest of your WordPress software.  And, if you like a particular plugin and want to support the developers, consider giving them a good review in the WordPress plugin list and see if perhaps they have a "donate" button in their plugin description there.

-----
### Updating and Security

Now that you have built your website it is time to look at how to secure and maintain it for the future. These can be big and off putting topics where it seems like you need to build an impenetrable fortress to defend against the whole internet. We are going to do the five minute version instead. This should get you through the most common obstacles and help you recover from any troubles you run into later on.

#### SPAM

SPAM is the most likely problem you will run into while running your own site.  Most of it comes in as comments because they are easy to post and it is easy to lose sight of what people are saying in comments, especially if they are commenting on older material you do not look at regularly. Turning on comment moderation means every comment will be emailed to you for approval before being posted to your site. Sign in to your site and go to your dashboard. The options you want are under "Settings --> Discussion". Make sure to check the boxes for "Email me whenever anyone posts a comment" and "Before a comment appears comment must be manually approved" so that your settings look like this: ![WordPress comment settings](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/sources/content/images/wp-comment-moderation.png)

Moderating every comment is not the default setting but I find it a good place to start with a new site. You may end up getting so many legitimate comments that moderating all of them is impractical or you may not want comments on your site at all. Experiment with different settings as your site grows and you see what kind of SPAM it attracts.

#### Accounts

By default WordPress is set up so that anyone who wants can create an account.  Some people prefer to use account as a SPAM control by making everyone who wants to post a comment register an account first.  However, since WordPress has better built-in comment management tools than user management tools, I prefer to moderate comments and have no other users. To turn off user registration open your site dashboard and go to "Settings --> General". Simple uncheck the box labeled "Anyone can register" box under "Menbership".

If you later decide to have people register on your site, for a course or other collaborative project, you can simply turn registration back on for a certain period of time when you will be paying attention to who registers and then turn it off again. If you plan to keep user registration on, consider a security plugin like the "[All In One WordPress Security and Firewall](https://www.tipsandtricks-hq.com/wordpress-security-and-firewall-plugin)", which has an option to require approval of new user registrations. 

#### Updates

Keep your software updated. Old software is easier for people to break and WordPress is so popular that there are many people out there who try and do just that, whether to post SPAM, steal email and password information, or for some other nefarious purpose. Thankfully there is also a great community of WordPress developers and users who report and fix these issues as they come up but the only way you can benefit from their hard work is to keep your software updated.  WordPress makes it easy to update your main software as well as any plugins and themes all from a single "updates" tab. You should log in at least every month to make sure everything is updated. Simply log in to your site dashboard and look for the "Updates" tab on the top of the left hand menu. When you have updates available a little orange circle will appear there telling you how many updates you have available like this:

![WordPress update status](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/sources/content/images/wp-dashboard-updates.png)

You can also have Reclaim do all this updating for you automatically. To turn on automatic updates:

* Log in to your Reclaim hosting account
* Navigate to the "cPanel" button,

![Reclaim Client area](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/sources/content/images/reclaim-client-area.png)

* Select your WordPress site in the application list

![cPanel application list](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/4054a49f1976dc2eb10615e8d9ae03193b9300df/content/images/cPanel-wordpress.png)

* Scroll down to the "Automatic Updates" options on the "My Application" tab that opens up

![](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/sources/content/images/cPanel-updates.png)

You can turn on updates for all versions or just for minor versions, which is a little more likely to be stable, and you can also update plugins and themes.  Be aware that WordPress updates, while very reliable, are not always perfect so updating automatically may cause parts of your site to break or start looking differently, especially between different major versions. This brings us to the last big point: backups.

#### Backups

Whatever happens to your site, you can always recover if you have a backup. Reclaim [automatically keeps 30 days of backups](https://reclaimhosting.com/backups-done-right/) for you so you are protected against anything that might go wrong on their servers. This can be a lifesaver. However, if you are not checking your site regularly, something might break and stay broken for longer than that month, in which case the automatic backups cannot help you. If you want more protection, and especially if you want to use the automatic upgrades mentioned in the previous section, you should turn on additional WordPress backups. This will allow you to keep backups on your schedule. You can turn on these backups in the same place as automatic upgrades, via cPanel. Just scroll right below the automatic updates area listed in the last part and you should see this: ![cPanel application backup options](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/sources/content/images/cPanel-backups.png)

How many backups you want depends on how regularly your site changes. For personal sites you are probably fine to skip daily and weekly backups entirely since Reclaim has a month worth of daily backups for you already.  I would recommend having 3 or more monthly backups, that way you can recover to the beginning of a semester if you need.

#### HTTPS

HTTPS is the secure way to connect to websites and it is made possible by a technology called SSL.  SSL keeps people on the same network as you, for instance on the wireless network at a coffee shop, from seeing your password when you log in to your site. This is especially important if you have other people logging in to your site or if you are using the same password for other sites. Setting this one up for yourself is actually a bit complicated but thankfully Reclaim will turn it on for you for free.  Just log in to your reclaim account, click on the "Open Ticket" ![Reclaim hosting "Open Ticket" button](https://raw.githubusercontent.com/edtechgarden/edtechgarden.github.io/sources/content/images/reclaim-open-ticket.png) button and tell them  "I would like a Let's Encrypt SSL certificate for my WordPress site please" and you should be all set.

#### Epilogue

If these security settings fail and your site is broken into or flooded with SPAM, never fear. Reclaim has a great article on how to [clean out your site](http://docs.reclaimhosting.com/wordpress/cleaning-a-hacked-wordpress-site) and restore from one of your backups.

