Stephen Smith -   Deployment Plan

Server Architecture

I will create a single HTML page for my portfolio site.  To do this I will employ a single-tier server with Apache.  
A second server will be used as a safe staging environment to give a "pre-view" of our site.

GitHub

 A main git repository will work in conjunction with both servers in the /var/www folder.   We will push the local repository up to the staging server.

Deployment Plan

Naming scheme for repos
	•	Production Repository: portfolio - server1
	•	Staging Repository: portfolio-staging

	
	1.	$ git checkout master
	1.	Switches to the local master branch
	2.	$ git pull github master
	1.	github is the name of the remote repo we will use to differentiate between our other remote deployment servers
	2.	Resolve any conflicts
	1.	Visit each conflicted file and resolve any conflicts. This will require a saving.
	1.	Once conflicts are resolved and saved, they need committed and another pull of remote is required.
	1.	$ git add -A
	2.	$ git commit -am ‘Relevant detailed commit message.’
	3.	$ git pull github master
	3.	$ git merge newFeatureName
	1.	Resolve any conflicts 
	4.	Test  You have just altered the code base since you last tested your new feature.  Beta test all functionality.
	
    $ git push github master
	1.	Push your changes up to the shared repo so that other dev’s can react to the latest changes to the project codebase.
