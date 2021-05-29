# Web development

## Miscellaneous

Understanding pixels and other CSS units
https://webplatform.github.io/docs/tutorials/understanding-css-units/

## Web design

https://webflow.com/designer


https://www.editorx.com/


https://www.figma.com/

## WordPress

Watch out for cheapskates, do maintenance contract.

Comment from: https://news.ycombinator.com/item?id=27311198#27318266

*"Personally, I think trying to apply modern development practice to wordpress development is a waste of time. You're going to fight an uphill battle. Instead, just treat it as a legacy platform and use legacy development methodology: have at least two or three copies of the site (dev, staging and production). Use sftp to live edit the code on dev/staging, then copy to production regularly. Make sure to have a versioned daily backup in place which at least can pull the last 7 days daily backup and the last 6 months monthly backups, and you're set. If your app is getting too complex for this development method, you can always switch back to django or other modern frameworks with modern tooling."*

*"I agree with this approach. Fortunately, there are managed services specifically for Wordpress that handle all this stuff. Cloudways, WPEngine, there are several others too. Cloudways lets you set up and manage WP using Digital Ocean, Vultr, AWS or GCP if I recall."*

*"I suggest going through the VIP docs as well as they have some really good advice on securing and speeding up wordpress along with what to avoid. https://docs.wpvip.com/technical-references/ Also just a tip: https://github.com/WordPress/WordPress-Coding-Standards"*

*"The professional approach is a local copy for development, a staging copy on hosting for QA, and then production. Code goes up in deployments; DB and files come down in regular synchronization. If there are multiple devs you might also have an integration copy on hosting. This is not specific to WP; I’ve seen the same workflow work for other DB-backed CMSs like Drupal."*

----

CI/CD Wordpress hosted

https://buddy.works/pricing
##### Wordmove https://github.com/welaika/wordmove

Wordmove is a command line tool that lets you automatically mirror local WordPress installations and DB data back and forth from your local development machine to one or more remote servers.


##### Wocker https://wocker.dev/

Docker in VM with Vagrant, but doesn't do anything with Virtual Private Server Instances (Like Digital Ocean)

##### Trellis Wordpress https://github.com/roots/trellis

Trellis is an open source project and completely free to use.
Can also utilize Digital Ocean

#### Varying Vagrant Vagrants https://github.com/Varying-Vagrant-Vagrants/VVV

VVV is a local developer environment, mainly aimed at WordPress developers. It uses Vagrant and VirtualBox, and can be used to build sites, and contribute to WordPress. With vagrant.

https://wecodemore.github.io/wpstarter/docs/what.html

####  Roots https://roots.io/

Roots helps you build better WordPress sites.

With Sage, Bedrock and Trellis.


#### WordPress Coding Standards for PHP_CodeSniffer 
https://github.com/WordPress/WordPress-Coding-Standards


This project is a collection of PHP_CodeSniffer rules (sniffs) to validate code developed for WordPress. It ensures code quality and adherence to coding conventions, especially the official WordPress Coding Standards.

Also checkout: https://github.com/WordPress

#### Corcel https://github.com/corcel/corcel

Corcel is a collection of PHP classes built on top of Eloquent ORM (from Laravel framework), that provides a fluent interface to connect and get data directly from a WordPress database.

You can use WordPress as the backend (administration panel) or CMS, for inserting posts, custom types, etc, and any other PHP app in the other side querying those data (as a Model layer). It's easier to use Corcel with Laravel, but you're free to use it with any PHP project that uses Composer.

#### Xdebug https://xdebug.org/
Xdebug is an extension for PHP, and provides a range of features to improve the PHP development experience.

#### ClassicPress https://www.classicpress.net/

Just an alternative don't know if it's better.

#### WP Sync DB – https://github.com/wp-sync-db/wp-sync-db
This WordPress plugin that lets you push, pull, and sync database tables between WordPress installations. WP Sync DB eliminates the manual work of migrating a WP database. Copy your db from one WP install to another with a single-click in your dashboard. This is especially handy for syncing a local development database with a live site.

roketco.com/log/the-ultimate-workflow-guide-for-teams-building-wordpress-sites-with-acf-timber-foundation-and-local-machines-with-remote-servers-through-vagrant-and-git/