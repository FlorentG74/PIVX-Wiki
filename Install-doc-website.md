Scope: website being delivered as part of the following proposal: https://forum.pivx.org/threads/doc-support-website.954/

Objective of this document is to
1/describe the technical architecture of the new pivx documentation website
2/explain the deployment procedure
3/list the deployment requirements

1. Technical architecture
* The website is based on the Grav CMS (https://getgrav.org/)
* The theme and templates are custom and have been implemented by Palmtree and I
* the website is entirely file-based. All it needs to run is PHP.
* It only uses basic functionalities so there will be no access to admin page etc, limiting security risks.
* Website core and content are stored on 2 separate git repos. Content is public, core is private.
* A test instance (WIP) of the website is available at this link: https://p558.phpnet.org/pivx_doc

2. Deployment procedure
* On the webserver add the token to the core website GitHub (to be provided later)
* On the web server, in a new folder, run 'git clone --recurse-submodules --remote-submodules https://github.com/FlorentG74/PIVX-Doc-Core-Website pivx_doc/'
* Add the following entry in crontab (adapt path to webserver folder structure): '*/5 * * * * cd www/pivx_doc/user/pages/content/ && git pull origin main'
* That's it! Website content will autoupdate every 5 mins

3. Requirements
* A new subdomain on the pivx.org domain. Proposal: docs.pivx.org
* A new folder on a webserver where the site can be hosted. The webserver will need to have PHP and git available
Once the website will be live there will be some cleanup required on the forum, and new links to be created on the website but we can look into it as a second step

